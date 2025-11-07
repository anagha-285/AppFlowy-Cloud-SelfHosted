
# AppFlowy Cloud — Self-Hosted Deployment

## 🧩 Overview
This project demonstrates a full **self-hosted deployment** of AppFlowy Cloud, including its **native application backend, authentication, database, cache, storage, and admin UI**.  
It enables collaboration, file storage, and user management in a production-like environment.

---

## 🧱 Architecture

| Component | Description | Port | Dependencies |
|-----------|-------------|------|---------------|
| Postgres | Database | 5432 | None |
| Redis | Session cache | 6379 | None |
| Minio | File storage (S3 compatible) | 9000 | None |
| GoTrue | Auth server | 9999 | Postgres |
| AppFlowy-Cloud | Core backend API | 8000 | GoTrue, Postgres, Redis, Minio |
| User Admin UI | Admin and user management | 8080 | GoTrue, Redis |
| PgAdmin | DB monitoring | 5050 | Postgres |
| Portainer | Docker management | 9443 | Docker socket |

---

## ⚙️ Setup Instructions

1️⃣ **Clone Repository**
```bash
git clone https://github.com/<username>/AppFlowy-Cloud-SelfHosted.git
cd AppFlowy-Cloud-SelfHosted
