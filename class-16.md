# Class 16 - Serverless Functions

## What are the key characteristics of serverless computing, and how does it differ from traditional server-based architectures?

The key characteristics of serverless computing are:

- No server management
- Flexible scaling
- Automated high availability
- No idle capacity
- Reduced costs

and it differ from traditional server-based architectures in the way that it is a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers. A serverless application runs in stateless compute containers that are event-triggered, ephemeral (may last for one invocation), and fully managed by the cloud provider. Pricing is based on the number of executions rather than pre-purchased compute capacity.

## How can one get started with Vercel, and what are the main steps involved in deploying a serverless function using Vercel?

- Create your project with an API Directory
- Create a handler class that derives from `BaseHTTPRequestHandler` and implement the `do_GET` method
- Deploy your project with Vercel
  - create github repo
  - push code to github
  - link github repo to vercel

## What are APIs, and how can they be utilized in Python applications to access and manipulate data from external sources?

An API (Application Programming Interface) is a set of functions that allows applications to access data and interact with external software components, operating systems, or microservices. To simplify, an API delivers a user response to a system and sends the system's response back to a user.

## What is the Requests library in Python, and how can it be used to interact with APIs by sending HTTP requests? Can you provide an example of a basic GET request using the Requests library?

The requests library is the standard for making HTTP requests in Python. It abstracts the complexities of making requests behind simple API so that you can focus on interacting with services and consuming data in your application.

```python
import requests

response = requests.get('https://api.github.com')
```
