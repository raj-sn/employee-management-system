# Learning Journey

## Project Goal

Build a containerized Employee Management System and deploy it to AWS using modern DevOps practices.

---

## Technologies Learned

### Application Development

- Python
- Flask
- HTML Templates
- CRUD Operations

### Database

- PostgreSQL
- SQL Queries
- Database Connectivity

### Containerization

- Docker Images
- Docker Containers
- Docker Networks
- Docker Volumes
- Docker Compose

### Version Control

- Git
- GitHub
- Branch Management
- Commit History

### CI/CD

- GitHub Actions
- Automated Deployment
- SSH-Based Deployment

### Cloud

- AWS EC2
- Linux Server Administration
- Security Groups

---

## Challenges Faced

### Docker Networking

Learned how containers communicate through Docker Compose service names.

### PostgreSQL Volume Issues

Resolved data volume conflicts and understood persistent storage concepts.

### GitHub Authentication

Fixed account and credential-related issues during GitHub integration.

### Deployment Automation

Configured GitHub Actions to automatically deploy the application to AWS EC2.

### Git History Divergence

Learned how force pushes affect deployment servers and why:

```bash
git fetch origin
git reset --hard origin/main
```

is better than:

```bash
git pull
```

for deployment environments.

---

## Skills Gained

- Linux Command Line
- Docker & Docker Compose
- AWS EC2 Deployment
- GitHub Actions
- CI/CD Pipelines
- PostgreSQL
- Flask Development
- Troubleshooting & Debugging

---

## Project Outcome

Successfully developed, containerized, deployed, and automated an Employee Management System using:

- Flask
- PostgreSQL
- Docker
- GitHub Actions
- AWS EC2

The project provided hands-on experience with real-world DevOps workflows and cloud deployment practices.

---

## Next Learning Goals

- Nginx Reverse Proxy
- HTTPS (Let's Encrypt)
- Docker Hub / Amazon ECR
- Amazon ECS
- Terraform
- Kubernetes