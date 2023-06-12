# Class 27 - Django Models

## Explain the purpose and basic structure of Django models. How do they help in creating and managing database schema in a Django application?

Django web applications access and manage data through Python objects referred to as models. Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms, etc. The definition of the model is independent of the underlying database — you can choose one of several as part of your project settings. Once you've chosen what database you want to use, you don't need to talk to it directly at all — you just write your model structure and other code, and Django handles all the dirty work of communicating with the database for you.

```python
from django.db import models

class Person(models.Model):
    first_name = models.CharField(max_length=30)
    last_name = models.CharField(max_length=30)

```

## Describe the primary features and functionality of the Django Admin interface. How can it be customized to suit the specific needs of a project?

The Django admin application can use your models to automatically build a site area that you can use to create, view, update, and delete records. This can save you a lot of time during development, making it very easy to test your models and get a feel for whether you have the right data. The admin application can also be useful for managing data in production, depending on the type of website. The Django project recommends it only for internal data management (i.e. just for use by admins, or people internal to your organization), as the model-centric approach is not necessarily the best possible interface for all users, and exposes a lot of unnecessary detail about the models.

You can further customize the interface to make it even easier to use. Some of the things you can do are:

- List views:
    Add additional fields/information displayed for each record.
    Add filters to select which records are listed, based on date or some other selection value (e.g. Book loan status).
    Add additional options to the actions menu in list views and choose where this menu is displayed on the form.
- Detail views
    Choose which fields to display (or exclude), along with their order, grouping, whether they are editable, the widget used, orientation etc.
    Add related fields to a record to allow inline editing (e.g. add the ability to add and edit book records while you're creating their author record).

## Briefly outline the key components and workflow of a Django application, as discussed in the Beginner’s Guide to Django. How do these components interact with each other to create a functional web application?

The key components of Django are:

- Model: which is the data layer, it is the database that contains the data that the user will interact with.

- View: which is the logic layer, it is the layer that contains the logic of the application, and it is the layer that connects the model and the template.

- Template: which is the presentation layer, it is the layer that contains the HTML files that will be rendered to the user.

Django follows the MVC (Model-View-Controller) pattern, but it is called MTV (Model-Template-View) in Django, and it is a software design pattern for developing a web application, it's role is to separate the logic of the application from the presentation of the application.

The workflow of a Django application is:

- The user sends a request to the Django application.

- The Django application sends the request to the URL dispatcher.

- The URL dispatcher sends the request to the view.

- The view sends the request to the model.

- The model sends the request to the database.  

- The database sends the response to the model.

- The model sends the response to the view.

- The view sends the response to the template.

- The template sends the response to the user.
