# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Build a REST API with FastAPI to manage tasks. Practice defining endpoints, handling JSON requests and responses, validating data with Pydantic, and using appropriate HTTP status codes.

## 📝 Tasks

### 🛠️ Create the API and Read Endpoints

#### Description
Create a Python application with FastAPI that manages a collection of tasks in memory. Start by adding a health-check endpoint and endpoints for listing tasks and retrieving one task by its ID.

#### Requirements
The completed application must:

- Install FastAPI and Uvicorn and run the application with Uvicorn
- Define a task with an integer `id`, a `title`, and a boolean `completed` field
- Return `{"status": "ok"}` from `GET /health`
- Return the task collection from `GET /tasks`
- Return one task from `GET /tasks/{task_id}`, or HTTP `404` when the ID does not exist

### 🛠️ Implement Create, Update, and Delete Operations

#### Description
Expand the API to support the complete set of CRUD operations for tasks. Keep the data in memory; a database is not required.

#### Requirements
The completed application must:

- Create a task with `POST /tasks` and return HTTP `201` with the created task
- Update an existing task with `PUT /tasks/{task_id}`
- Delete an existing task with `DELETE /tasks/{task_id}` and return HTTP `204`
- Return HTTP `404` when an update or delete request targets a task that does not exist
- Keep the task collection consistent after each create, update, and delete request

### 🛠️ Validate Requests and Test the API

#### Description
Add request validation and verify that the API behaves correctly for both valid and invalid requests. Use FastAPI's interactive documentation to explore and test the endpoints.

#### Requirements
The completed application must:

- Use Pydantic request models to validate task data
- Reject a task with a missing or blank title
- Return clear, appropriate HTTP status codes for successful and unsuccessful requests
- Test the health check and each CRUD operation using `/docs` or an HTTP client
- Confirm that invalid input and unknown task IDs produce error responses rather than successful task data
