# System Architecture

## Overview

The Employee Management System is a containerized web application built using Flask and PostgreSQL. The application is deployed on AWS EC2 using Docker Compose and automatically updated through a GitHub Actions CI/CD pipeline.

## Architecture Diagram

../Diagram/project-architecture.png

## Components

### Flask Application

The Flask application provides:

- Employee management operations
- Web interface
- Database connectivity
- CRUD functionality

### PostgreSQL Database

The PostgreSQL database stores:

- Employee records
- Employee details
- Persistent application data

### Docker Compose

Docker Compose manages:

- Flask container
- PostgreSQL container
- Container networking
- Volume management

### GitHub Actions

GitHub Actions provides:

- Continuous Integration (CI)
- Continuous Deployment (CD)
- Automated deployment to AWS EC2

### AWS EC2

AWS EC2 hosts:

- Docker Engine
- Docker Compose
- Flask application container
- PostgreSQL container

## Deployment Architecture

Developer
→ GitHub Repository
→ GitHub Actions
→ AWS EC2
→ Docker Compose
→ Flask + PostgreSQL

## Networking

The Flask and PostgreSQL containers communicate through a Docker network.

Communication Flow:

Flask Container
↔ Docker Network
↔ PostgreSQL Container

## Data Persistence

PostgreSQL data is stored using Docker volumes to ensure data remains available even if containers are recreated.