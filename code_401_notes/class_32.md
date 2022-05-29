# Code 401 Reading Notes 
### 32. Permissions & PostgreSQL 

####  source: "Permissions" [link](https://www.django-rest-framework.org/api-guide/permissions/)
- permission checks run at the start of a view, before other code 
- these often use the request.user and request.auth properties 
  - ex: "IsAuthenticated" class in the Django REST framework  
- if a permission check fails, exceptions will be raised and the view will not run 
- in addition to view-level permissions, there are also object-level permisisons 

```python 
# default permission policy, set globally: 
'DEFAULT_PERMISSION_CLASSES': [
   'rest_framework.permissions.AllowAny',
]

# more specific permissions in a views.py tell Django to ignore the settings.py file default  
# permissions set for a class-based view: 
from rest_framework.permissions import IsAuthenticated
from rest_framework.response import Response
from rest_framework.views import APIView

class ExampleView(APIView):
    permission_classes = [IsAuthenticated]

    def get(self, request, format=None):
        content = {
            'status': 'request was permitted'
        }
        return Response(content)
```

- class that covers both authentication AND authorization: 
  - DjangoModelPermissions class 

#### Things I want to know more about 
- I'm still a bit unsure how to do the typical authorizaiton setup with classes
