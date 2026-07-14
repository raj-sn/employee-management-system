# Employee Management System

A simple Employee Management System built using:

- Flask
- PostgreSQL
- Docker
- Docker Compose

## Features

- Add Employee
- View Employees
- Delete Employee
- PostgreSQL Database
- Dockerized Application

## Technology Stack

- Python
- Flask
- PostgreSQL
- Docker
- Docker Compose
- Git
- GitHub

## Project Structure

```text
employee-management-system
│
├── app.py
├── db.py
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── templates
│   └── index.html
└── README.md
```

## Run Locally

```bash
docker compose up --build
```

Open:

```text
http://localhost:5000
```

## Database

```text
PostgreSQL
```

Database Name:

```text
employee_db
```

## Architecture

```text
Browser
   ↓
Flask Container
   ↓
Docker Network
   ↓
PostgreSQL Container
   ↓
Docker Volume
```

## CI Pipeline

```text
Developer
    ↓
Git Push
    ↓
GitHub Actions
    ↓
Docker Build
    ↓
Success / Failure
```


## Author

Raj S.N.
