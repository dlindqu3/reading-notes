# Code 401 Reading Notes 
### 26. Intro to Django 

####  source: "Getting started with Django" [link](https://www.djangoproject.com/start/)
- Object-relational mapper: set up models of sql data using classes within .py files
- URLS and views: create a URLconf file, with a list of "urlpatterns"; in another file, define a function to render material to that URL 
- Templates: Django using jinja templating 
- forms: create with Django's forms library 
- authentication: built in to Django, from django.contrib.auth.decorators
- Admin: manage content on site via metadata of models  

####  source: William Vincent, "How Django Works Behind the Scenes" [link](https://wsvincent.com/how-django-works-behind-the-scenes/)
- Django is run by a non-profit 
- Django's code is open source 
- one easy way to get involved in the community is to attend a DjangoCon 


#### Things I want to know more about 
- How to host a django + sql project. does hosting a django backend on something like heroku automatically host the attached sql database as well? Or are there extra steps? 