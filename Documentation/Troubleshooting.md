# Troubleshooting Guide

This document records common issues encountered during project development and deployment.

---

## 1. PostgreSQL Container Not Starting

### Issue

PostgreSQL container exited immediately after startup.

### Cause

Old Docker volume data conflicted with the PostgreSQL image version.

### Solution

```bash
docker compose down
docker volume rm <volume_name>
docker compose up --build
```

---

## 2. Flask Could Not Connect To PostgreSQL

### Issue

Flask application failed to connect to the database.

### Cause

Incorrect database host configuration.

### Solution

Use the Docker Compose service name:

```python
host="postgres-db"
```

instead of:

```python
host="localhost"
```

---

## 3. GitHub Authentication Error

### Issue

Unable to push code to GitHub.

### Cause

Old GitHub credentials were stored locally.

### Solution

```powershell
"protocol=https`nhost=github.com" |
git credential-manager erase
```

Then sign in again with the correct GitHub account.

---

## 4. EC2 Deployment Not Updating

### Issue

GitHub Actions completed successfully, but the website showed old content.

### Cause

Git history divergence caused by force push and hard reset operations.

### Solution

Replace:

```bash
git pull
```

with:

```bash
git fetch origin
git reset --hard origin/main
```

---

## 5. EC2 SSH Access Issues

### Issue

Unable to connect to EC2.

### Cause

AWS Security Group was not configured correctly.

### Solution

Allow:

- SSH (Port 22)
- Custom TCP 5000 (Application Access)

in the EC2 Security Group.

---

## 6. Docker Container Troubleshooting

### Check Running Containers

```bash
docker ps
```

### View Container Logs

```bash
docker logs flask-app
docker logs postgres-db
```

---

## Key Lessons Learned

- Docker networking using service names
- Docker volumes and data persistence
- GitHub credential management
- GitHub Actions deployment automation
- AWS EC2 server management
- Handling divergent Git branches during deployment