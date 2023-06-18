# Class 28 - Django CRUD and Forms

## How do Django Forms facilitate user input handling, and what are some key components of creating a form using the Django framework?

Forms are a flexible mechanism for collecting user input because there are suitable widgets for entering many different types of data, including text boxes, checkboxes, radio buttons, date pickers and so on.

Django provides a range of tools and libraries to help you build forms to accept input from site visitors, and then process and respond to the input.

## Explain the purpose of Django Templates in web development and describe how template inheritance can be utilized to improve code reusability and maintainability

A template is a text file defining the structure or layout of a file (such as an HTML page), with placeholders used to represent actual content. A template is rendered with specific data to produce a final document. Django templates provide a way to generate HTML dynamically, and can be used to create HTML forms for submitting data to the server.

Template inheritance allows you to build a base “skeleton” template that contains all the common elements of your site and defines blocks that child templates can override.

## Describe the function of Django Views in handling HTTP requests, and outline the differences between function-based views and class-based views

A view function, or view for short, is a Python function that takes a Web request and returns a Web response. This response can be the HTML contents of a Web page, or a redirect, or a 404 error, or an XML document, or an image . . . or anything, really. The view itself contains whatever arbitrary logic is necessary to return that response. This code can live anywhere you want, as long as it’s on your Python path. There’s no other requirement–no “magic,” so to speak. For the sake of putting the code somewhere, the convention is to put views in a file called views.py, placed in your project or application directory.

Function-based views are the original view type in Django, and are still the most commonly-used type. They are created by defining a function that accepts an HttpRequest object and returns an HttpResponse object.

Class-based views are an alternative way to implement views as Python objects instead of functions. They do not replace function-based views, but have certain differences and advantages when compared to function-based views.
