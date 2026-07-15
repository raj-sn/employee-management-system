# Cost Analysis

## Project Overview

This project was developed using AWS EC2, Docker, Docker Compose, GitHub Actions, Flask, and PostgreSQL.

The primary goal was to build and deploy a DevOps-based application while minimizing infrastructure costs.

---

## Infrastructure Components

### AWS EC2

Instance Type:

```text
t2.micro
```

Purpose:

- Host Flask application
- Host PostgreSQL database
- Run Docker and Docker Compose

Cost:

```text
AWS Free Tier Eligible
```

Estimated Monthly Cost After Free Tier:

```text
$8 - $12 USD/month
```

---

### GitHub

Services Used:

- GitHub Repository
- GitHub Actions

Cost:

```text
Free
```

For personal and educational projects, GitHub's free plan is sufficient.

---

### Docker

Services Used:

- Docker Engine
- Docker Compose

Cost:

```text
Free
```

---

### PostgreSQL

Deployment Method:

```text
PostgreSQL Docker Container
```

Additional Cost:

```text
None
```

The database runs within the EC2 instance.

---

## Estimated Monthly Cost

| Component | Estimated Cost |
|------------|---------------|
| AWS EC2 (Free Tier) | $0 |
| GitHub | $0 |
| Docker | $0 |
| PostgreSQL | $0 |

### Total During Free Tier

```text
$0/month
```

### Total After Free Tier

```text
Approximately $8 - $12 USD/month
```

---

## Cost Optimization Techniques

### Containerization

Docker allows multiple services to run on a single EC2 instance, reducing infrastructure costs.

### Free GitHub Actions

The project uses GitHub's free CI/CD features instead of paid DevOps tools.

### Single Server Deployment

Both Flask and PostgreSQL run on the same EC2 instance, minimizing cloud resource usage.

---

## Business Value

This project demonstrates how a complete CI/CD pipeline can be implemented using mostly free-tier resources while still following modern DevOps practices.

Key capabilities achieved:

- Automated CI/CD
- Cloud Deployment
- Containerization
- Source Control Integration
- Infrastructure Cost Awareness

---

## Conclusion

The project successfully delivers a production-style deployment workflow using low-cost cloud resources.

For learning, internship preparation, and portfolio purposes, the total operational cost remains close to zero while providing hands-on experience with real DevOps tools and practices.
``