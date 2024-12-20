# FastAPI - A Modern Web Framework for Building APIs

## What is FastAPI?

FastAPI is a modern web framework for building APIs with Python 3.7+ based on standard Python-type hints. It is known for being fast and helping developers by automatically producing documentation for their web services, making it easy for other developers to understand and use the API. FastAPI reduces human errors, speeds up development, and is production-ready. It is fully compatible with popular API standards such as OpenAPI and JSON schema.

## Features of FastAPI

- **Automatic Documentation**: FastAPI generates interactive API documentation automatically using the OpenAPI standard. You can access this documentation by visiting a specific endpoint in your application.
  
- **Python Type Hints**: FastAPI uses Python-type hints to annotate function parameters and return types, improving code readability and enabling automatic data validation.

- **Data Validation**: FastAPI uses Pydantic models for data validation, ensuring that incoming data is automatically validated, serialized, and deserialized.

- **Asynchronous Support**: FastAPI fully supports asynchronous operations, making it suitable for handling I/O-bound tasks and improving the responsiveness of your application.

- **Dependency Injection**: FastAPI supports dependency injection, allowing you to declare dependencies like database connections and authentication for your endpoints, making the code modular and maintainable.

- **Security Features**: FastAPI includes built-in security features like OAuth2, JWT, and automatic validation to prevent security vulnerabilities such as SQL injection and XSS attacks.

## Installation and Setup of FastAPI

To get started with FastAPI, follow these steps:

1. Install Python 3 if you haven’t already.
2. Install FastAPI using the following command:

    ```bash
    pip install fastapi
    ```


## Create a Simple API

Here’s how you can create a simple API that says "Hello" when you visit a specific web address. Save this code in a file, e.g., `main.py`.

```python
from fastapi import FastAPI

# Create a FastAPI application
app = FastAPI()

# Define a route at the root web address ("/")
@app.get("/")
def read_root():
    return {"message": "Hello, FastAPI!"}
```



To run the application, use the following command in the terminal:
```terminal
fastapi dev main.py
```

Once the application is running, open your browser and visit:
```
http://localhost:8000/
```
You should see the following response in your browser or an API testing tool like curl or Postman:
```
{"message": "Hello, FastAPI!"}
```
## Advantages of FastAPI
Here are some key advantages of using FastAPI:

- **Easy to Learn and Use**: FastAPI's simple syntax and automatic documentation generation make it easy for Python developers to get started.

- **High Performance** : FastAPI is one of the fastest Python web frameworks due to its asynchronous support and efficient data handling.

- **Automatic Data Validation**: FastAPI automatically validates incoming data based on Python type hints, reducing errors caused by incorrect input.

- **Authentication and Authorization**: FastAPI offers simple methods for handling authentication and authorization, using OAuth2, JWT tokens, or custom methods.

- **Middleware**: You can easily add middleware to your FastAPI application for tasks like logging, authentication, or modifying requests/responses.
