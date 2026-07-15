# CI/CD Pipeline

## Overview

This project uses GitHub Actions to automatically deploy the application to AWS EC2 whenever code is pushed to the main branch.

## Pipeline Flow

```text
Developer
    ↓
Git Push
    ↓
GitHub Repository
    ↓
GitHub Actions
    ↓
AWS EC2
    ↓
Docker Compose
    ↓
Flask + PostgreSQL
```

## Deployment Process

### 1. Push Code

```bash
git add .
git commit -m "Update application"
git push origin main
```

### 2. GitHub Actions Starts

GitHub automatically triggers the deployment workflow.

### 3. Connect to EC2

GitHub Actions uses SSH to connect to the AWS EC2 instance.

### 4. Update Application

```bash
git fetch origin
git reset --hard origin/main

sudo docker compose up -d --build
```

### 5. Application Updated

The latest version becomes available on the EC2 server.

---

## GitHub Actions Workflow

```yaml
name: Deploy

on:
  push:
    branches:
      - main
```

Whenever code is pushed to the main branch, deployment starts automatically.

---

## Benefits

- Automated deployment
- Faster updates
- Reduced manual work
- Consistent deployments

---

## Skills Learned

- GitHub Actions
- CI/CD Pipelines
- AWS EC2
- SSH Deployment
- Docker Compose
- Git Automation