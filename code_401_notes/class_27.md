# Code 401 Reading Notes 
### 27. Django Models  

####  source: "Django Tutorial Part 3: Using models" [link](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models)
- Models define the structure and type of stored data 
- You can choose various database types to fit a given model 
- an "object" is a group of related info (for a book website example, objects might include books, book instances, genre, and authors)
- Django allows you to define relationships that are one to one, one to many, and many to many 
-typical setup example: 

```python 
from django.db import models
from django.urls import reverse

class MyModelName(models.Model):
    """A typical class defining a model, derived from the Model class."""

    # Fields
    my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')
    ...

    # Metadata
    class Meta:
        ordering = ['-my_field_name']

    # Methods
    def get_absolute_url(self):
        """Returns the URL to access a particular instance of MyModelName."""
        return reverse('model-detail-view', args=[str(self.id)])

    def __str__(self):
        """String for representing the MyModelName object (in Admin site etc.)."""
        return self.my_field_name
```

- creating an accessing data: 

```python 
# Create a new record using the model's constructor.
record = MyModelName(my_field_name="Instance #1")
# Save the object into the database.
record.save()
# Access model field values using Python attributes.
print(record.id) # should return 1 for the first record.
print(record.my_field_name) # should print 'Instance #1'
# Change record by modifying the fields, then calling save().
record.my_field_name = "New Instance Name"
record.save()
all_books = Book.objects.all()
wild_books = Book.objects.filter(title__contains='wild')
number_wild_books = wild_books.count()
# Will match on: Fiction, Science fiction, non-fiction etc.
books_containing_genre = Book.objects.filter(genre__name__icontains='fiction')
```

####  source: "Django Tutorial Part 4: Django admin site" [link](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Admin_site)
- we can now use the Django Admin site to add some "real" book data
- first register the models with the admin site
- then login and create some data
- a Django admin application can use your models to allow part of your site to create, view, update, and delete records
- to add your models to your admin application is to "register" them
- a "superuser" can then be used to create instances of models to test the site 

register models in admin.py: 
```python 
from django.contrib import admin

# Register your models here.
from .models import Author, Genre, Book, BookInstance

admin.site.register(Book)
admin.site.register(Author)
admin.site.register(Genre)
admin.site.register(BookInstance)
```

- create a superuser
- python3 manage.py createsuperuser
- python3 manage.py runserver
- login at the /admin URL (e.g. http://127.0.0.1:8000/admin) with new superuser userid and password 
- redirected back to /admin
- the admin page displays all our models, grouped by installed application
- you can click on a model to see all associated records
- you can "add" a record of a given type

#### Things I want to know more about 
- I don't understand the different types of "adding" books discussed in the "django tutorial part 4: admin" reading, in the "logging in and using the site" part of the page