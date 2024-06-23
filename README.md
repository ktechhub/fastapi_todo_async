<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/ktechhub/doctoc)*

<!---toc start-->

* [FastAPI TODO Async](#fastapi-todo-async)
  * [Database Deployment](#database-deployment)
  * [Blog Post](#blog-post)
  * [Features](#features)
  * [Requirements](#requirements)
  * [Installation](#installation)
  * [API Endpoints](#api-endpoints)
  * [Configuration](#configuration)
  * [License](#license)

<!---toc end-->

<!-- END doctoc generated TOC please keep comment here to allow auto update -->
# FastAPI TODO Async
This repository contains a TODO API built with FastAPI and SQLAlchemy, focusing on asynchronous programming for efficient performance.


## Database Deployment
```sh
docker run --name fastapi_todo_async -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=fastapi_todo_async -e MYSQL_USER=fastapi_todo_async -e MYSQL_PASSWORD=fastapi_todo_async -e MYSQL_DATABASE=fastapi_todo_async mysql:latest
```

## Blog Post
[https://www.ktechhub.com/tutorials/building-a-todo-api-with-fastapi-and-sqlalchemy-a-step-by-step-asynchronous-guide](https://www.ktechhub.com/tutorials/building-a-todo-api-with-fastapi-and-sqlalchemy-a-step-by-step-asynchronous-guide)


## Features

- **Asynchronous**: Utilizes FastAPI and SQLAlchemy's async capabilities for non-blocking operations.
- **CRUD Operations**: Implements Create, Read, Update, and Delete operations for TODO items.
- **Error Handling**: Uses HTTPException to manage error responses and validation using Pydantic schemas.
- **API Documentation**: Provides Swagger UI and ReDoc for interactive API documentation.

## Requirements

- Python 3.7+
- FastAPI
- SQLAlchemy

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/ktechhub/fastapi_todo_async.git
   cd fastapi_todo_async
   ```

2. Create a virtual environment:

   ```bash
   python -m venv env
   source env/bin/activate  # On Windows use `env\Scripts\activate`
   ```

3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```
4. Copy and update .env file
   ```bash
   cp .env.example .env
   ```
5. Set up the database configuration in `app/core/config.py`.

6. Run the FastAPI application:

   ```bash
   uvicorn app.main:app --reload
   ```

   Visit `http://localhost:8000/docs` for Swagger UI or `http://localhost:8000/redoc` for ReDoc.

## API Endpoints

- **POST `/todos/`**: Create a new TODO item.
- **GET `/todos/`**: Get all TODO items.
- **GET `/todos/{id}/`**: Get a TODO item by ID.
- **PUT `/todos/{id}/`**: Update a TODO item by ID.
- **DELETE `/todos/{id}/`**: Delete a TODO item by ID.

## Configuration

- Modify `app/core/config.py` to configure database settings (`DATABASE_URL`, etc.).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.