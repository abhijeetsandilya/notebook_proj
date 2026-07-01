#  fastapi-notes-api

A RESTful Notes Management API built using **FastAPI**, **PostgreSQL**, and **SQLAlchemy**. This project demonstrates backend application development with a relational database, request validation using Pydantic, and ORM-based database interactions while following a modular project structure.

---

## Overview

This project was developed to strengthen my understanding of modern backend development using Python. It implements a complete CRUD API for managing notes, integrating FastAPI with PostgreSQL through SQLAlchemy and using Pydantic for request validation.

---

## Features

* Create new notes
* Retrieve all notes
* Retrieve a note by its ID
* Update existing notes
* Delete notes
* PostgreSQL database integration
* SQLAlchemy ORM
* Request validation using Pydantic
* Interactive API documentation with Swagger UI and ReDoc

---

## Tech Stack

| Technology | Purpose              |
| ---------- | -------------------- |
| Python     | Programming Language |
| FastAPI    | Backend Framework    |
| PostgreSQL | Relational Database  |
| SQLAlchemy | ORM                  |
| Pydantic   | Data Validation      |
| Uvicorn    | ASGI Server          |

---

## Project Structure

```text
NotesAPI/
│
├── main.py             # API routes
├── database.py         # Database configuration
├── db_models.py        # SQLAlchemy models
├── model.py            # Pydantic schemas
├── requirements.txt
├── README.md
└── ...
```

---

## Installation

### 1. Clone the repository

```bash
git clone <repository-url>
cd fastapi-notes-api
```

### 2. Create a virtual environment

**Windows**

```bash
python -m venv venv
venv\Scripts\activate
```

**Linux / macOS**

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## Database Configuration

Create a PostgreSQL database and update the connection string in `database.py`.

Example:

```python
DATABASE_URL = "postgresql://username:password@localhost:5432/notes_db"
```

---

## Running the Application

Start the development server:

```bash
uvicorn main:app --reload
```

The API will be available at:

```
http://127.0.0.1:8000
```

---

## API Documentation

FastAPI automatically generates interactive API documentation.

### Swagger UI

```
http://127.0.0.1:8000/docs
```

### ReDoc

```
http://127.0.0.1:8000/redoc
```

---

## API Endpoints

| Method | Endpoint      | Description             |
| ------ | ------------- | ----------------------- |
| GET    | `/`           | Home endpoint           |
| GET    | `/notes`      | Retrieve all notes      |
| GET    | `/notes/{id}` | Retrieve a single note  |
| POST   | `/notes`      | Create a new note       |
| PATCH  | `/notes/{id}` | Update an existing note |
| DELETE | `/notes/{id}` | Delete a note           |

> *Endpoint names may vary slightly depending on the implementation.*

---

## Example Request

```json
{
    "title": "Meeting Notes",
    "content": "Discuss API development roadmap."
}
```

---

## Learning Outcomes

Through this project, I gained practical experience with:

* REST API design
* FastAPI
* PostgreSQL
* SQLAlchemy ORM
* Pydantic data validation
* CRUD application development
* Database session management
* Backend project organization

---

## Known Limitation

The current `PATCH` implementation replaces the entire note content during updates. This behavior is sufficient for the current project scope but could be refined in future iterations.

---

## Project Status

The current version implements the backend API and database layer. Additional improvements may be explored in future iterations as I continue learning and building.