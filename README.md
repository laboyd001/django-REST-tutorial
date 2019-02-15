# django-REST-tutorial
Repo for the Django REST tutorial


## Tutorial 1: Serialization
### Introduction
This tutorial will cover creating a simple pastebin code highlighting Web API. 
Along the way it will introduce the various components that make up REST framework, 
and give you a comprehensive understanding of how everything fits together.

The tutorial is fairly in-depth, so you should probably get a cookie and a cup of your favorite brew before getting started. 
If you just want a quick overview, you should head over to the quickstart documentation instead.


## Tutorial 2: Requests and Responses
From this point we're going to really start covering the core of REST framework. Let's introduce a couple of essential building blocks.

### Request objects
REST framework introduces a Request object that extends the regular HttpRequest, and provides more flexible request parsing. The core functionality of the Request object is the request.data attribute, which is similar to request.POST, but more useful for working with Web APIs.

`request.POST  # Only handles form data.`  Only works for 'POST' method.
`request.data  # Handles arbitrary data.`  Works for 'POST', 'PUT' and 'PATCH' methods.
### Response objects
REST framework also introduces a Response object, which is a type of TemplateResponse that takes unrendered content and uses content negotiation to determine the correct content type to return to the client.

`return Response(data)  # Renders to content type as requested by the client.`
### Status codes
Using numeric HTTP status codes in your views doesn't always make for obvious reading, and it's easy to not notice if you get an error code wrong. REST framework provides more explicit identifiers for each status code, such as `HTTP_400_BAD_REQUEST` in the status module. It's a good idea to use these throughout rather than using numeric identifiers.
