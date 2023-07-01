# Class 31 - Django REST Framework & Docker

## What are the key components of a Docker container, and how do they help streamline the development and deployment of applications?

Key components of a Docker container:

- Dockerfile: a text file that contains all the commands a user could call on the command line to assemble an image.
- Docker images: read-only templates that contain a set of instructions for creating a container that can run on the Docker platform.
- Docker daemon: a background service that manages the running containers.
- Docker registry: a repository for Docker images. Docker Hub is a public registry that anyone can use, and Docker is configured to look for images on Docker Hub by default.

they help streamline the development and deployment of applications by:

- Docker containers are lightweight and contain everything needed to run the application, so you can move them from one machine to another.

- Docker containers are isolated from one another and use resource isolation to prevent them from interfering with each other.

- Docker containers are portable because they can run on any machine with Docker installed, regardless of the underlying operating system.

- Docker containers are secure because they are isolated from each other and the underlying host system.

So Docker is a way to isolate and run entire applications. With Docker it doesn’t matter if you are using a Mac, Windows, or Linux computer anymore. The entire development environment is isolated: programming language, software packages, databases, and more.

With Docker we now longer have to mess around with virtual environments. We can faithfully reproduce a production environment locally. And Docker can be shared among team members so everyone is working on the same setup. Wins all around.

## Describe the primary steps involved in building a library website using Django, including essential components like models, views, and templates

- Set up the project directory and virtual environment.
- Install Django using pip.
- Create a new Django project using the startproject command.
- Create a new app within the project using the startapp command.
- Define a model for the app in the models.py file.
- Generate and apply migrations for the model using the makemigrations and migrate commands.
- Register the model in the admin site in the admin.py file.
- Create a view for listing books in the views.py file.
- Configure URLs for the project and the app.
- Create a template for displaying the book list.
- Run the local server and visit the website to see the book list.
- Write tests for the model, view, and template in the tests.py file.
- Run the tests using the test command.

## Can you explain the primary differences between Django and Django REST framework?

The most important deference is that Django creates websites containing webpages, while Django REST Framework creates web APIs which are a collection of URL endpoints containing available HTTP verbs that return JSON.

Django REST framework is a powerful and flexible toolkit for building Web APIs. Django REST framework is a third-party package, built and maintained by a dedicated team of volunteers. It's mature, reliable, and well-tested. Django REST framework is used to build APIs for web applications and for mobile and IoT devices, and can be used with most databases.
