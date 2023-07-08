# Class 33: Authentication & Production Server

## What is the primary purpose of JSON Web Tokens (JWTs) and how do they work in terms of encoding and decoding data?

JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

## How does JWT Authentication integrate with Django REST Framework to secure API endpoints, and what are the key components involved in this process?

The most common way to use JWTs in Django REST Framework is to use the provided JSONWebTokenAuthentication authentication class. This authentication class will attempt to authenticate against a given request using JWT-based authentication. The way it works is as follows:

- the client sends their credentials (username and password) to the server
- the server authenticates the credentials and returns a refresh and an access token
- access token is sent by the client to the server
- server decodes the token and verifies it’s signature
- if everything checks out, the server returns a protected resource

## Why is Django’s built-in runserver not suitable for production environments, and what are some alternative server options that should be considered for deploying a Django application?

the server started with runserver is not guaranteed to be performant (it’s very slow), and it hasn’t been built with security concerns in mind. Not a good fit for production use.

Some alternative:

- Gunicorn (Green Unicorn) is a widely used WSGI server that can handle multiple simultaneous requests and provides good performance. It integrates well with Django and supports features like worker processes, process management, and graceful restarts.

- uWSGI is another commonly used WSGI server that supports various protocols and can serve thousands of requests simultaneously. It also provides process management, which allows you to perform actions like reloading the application without dropping any requests.

- Nginx is a popular web server that can also be used as a reverse proxy, load balancer, mail proxy, and HTTP cache. It’s often used in combination with Gunicorn or uWSGI to serve Django applications in production environments.

- Docker-based deployment: Docker allows packaging the Django application with its dependencies into containers, providing a portable and isolated deployment. It enables deploying Django applications using various server options while ensuring consistency across different environments.
