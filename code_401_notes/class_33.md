# Code 401 Reading Notes 
### 33. Authentication & Production Server 

####  source: "Introduction to JSON Web Tokens" [link](https://jwt.io/introduction/)
- this is an open standard for transfering data as JSON between two parties 
- the data can be signed using a secret or a public/private key pair 
- common usages of JWT: 
  - authorization for user login and subsequent activities
  - info exchange 
- a typical JSON web token consists of three parts: header.payload.signature 
- payload contains claims, of which there are three types - registered, public, and private 
- a signature signs a header and payload 
-placement of token in header: 
  - "Authorization: Bearer <token>" (this should stop CORS-related problems)

####  source: Vitor Freitas, "How to Use JWT Authentication with Django REST Framework" [link](https://simpleisbetterthancomplex.com/tutorial/2018/12/19/how-to-use-jwt-authentication-with-django-rest-framework.html)
- this article covers BACKEND auth 
- the JWT should be included in all requests 
- the JWT comes from switching a username/passworkd for an access & refresh tokens 
- a backend can send then send a signature, using the header base64 + payload base64 + SECRET_KEY 
- for django apps, here is the setup:

```python 
# pip install djangorestframework_simplejwt

# settings.py 
REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': [
        'rest_framework_simplejwt.authentication.JWTAuthentication',
    ],
}

# main urls.py 
from django.urls import path
from rest_framework_simplejwt import views as jwt_views

urlpatterns = [
    # Your URLs...
    path('api/token/', jwt_views.TokenObtainPairView.as_view(), name='token_obtain_pair'),
    path('api/token/refresh/', jwt_views.TokenRefreshView.as_view(), name='token_refresh'),
]

# views.py 
from rest_framework.views import APIView
from rest_framework.response import Response
from rest_framework.permissions import IsAuthenticated


class HelloView(APIView):
    permission_classes = (IsAuthenticated,)

    def get(self, request):
        content = {'message': 'Hello, World!'}
        return Response(content)

# urls.py 
from django.urls import path
from myapi.core import views

urlpatterns = [
    path('hello/', views.HelloView.as_view(), name='hello'),
]

```

- authenticate and obtain a token with a POST request to  /api/token/
- from this endpoint, grab the access and refresh tokens, and pass them to the frontend to store in local storage 
- to see protected views on the backend, include the access token in the header of requests
- to get a new access token, post to /api/token/refresh/refresh=<refresh token>

####  source: "Django Runserver Is Not Your Production Server" [link](https://vsupalov.com/django-runserver-in-production/)
- when your server gets a request, if the request is not for static content, the webserver should pass the request on to the next component 
- the next component is an application server
- your Django app does not run by just taking and responding to requests 
- Your project provides a uwsgi.py file, which contains a function to be called by the application server
- This function gets a Python object representing the incoming request
- This function calls your code, and produces a response object which is passed to the WSGI server
- There the response is translated into a HTTP response and is passed back to the web server, which finally delivers it to the user

####  source: "JSON Web Tokens With Django REST Framework" [link](https://www.youtube.com/watch?v=Fhcn2qx-4VQ)
- pip install djangorestframework_simplejwt
- pip install requests 

```python
# send.py 
import requests 

headers = {}
headers['Authorization'] = 'Bearer <access token>' 

r = requests.get('<endpoint>', headers=headers)
print(r.text)
```

#### Things I want to know more about 
- Is JWT a part of AuthO? Or are they just often used together? 
- I still don't really understand the different types of servers mentioned in the "Django Runserver Is Not Your Production Server" article 
- add DEFAULT_AUTHENTICATION_CLASSES to settings.py 
- 