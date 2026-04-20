# 🚀 MERN Task Manager App (Fullstack + DevOps)

A production-ready **Task Manager Application** built with the MERN stack and deployed using modern DevOps practices including **Docker, VPS, Nginx, and CI/CD automation**.

---

## 🧠 Tech Stack

### Frontend

* React.js
* Axios

### Backend

* Node.js
* Express.js
* MongoDB (MongoDB Atlas)

### DevOps

* Docker
* Docker Hub
* GitHub Actions (CI/CD)
* Nginx (Reverse Proxy)
* VPS (Ubuntu)

---

## ⚙️ Features

* 🔐 User Authentication (JWT)
* 📝 Task CRUD (Create, Read, Update, Delete)
* 🔒 Protected Routes
* 🌐 REST API
* 📦 Dockerized Backend
* 🚀 Auto Deploy CI/CD
* 🌍 Production-ready deployment

---

## 🏗️ Architecture

```
User → Nginx (Port 80)
         ↓
     Backend (Docker :5000)
         ↓
   MongoDB Atlas (Cloud DB)
```

---

## 🚀 Live Access

```
http://YOUR_VPS_IP
```

---

## 📦 Project Structure

```
TASK-MANAGER-APP/
│
├── backend/
│   ├── routes/
│   ├── models/
│   ├── app.js
│   └── Dockerfile
│
├── frontend/
│   ├── src/
│   └── build/
│
└── .github/workflows/
    └── deploy.yml
```

---

## 🐳 Docker Setup (Backend)

### Build Image

```bash
docker build -t backend-app ./backend
```

### Run Container

```bash
docker run -d -p 5000:5000 \
--env-file .env \
-e NODE_ENV=production \
--name backend backend-app
```

---

## ☁️ Deployment (VPS)

* VPS: Ubuntu 22.04
* Docker installed
* Nginx configured as reverse proxy

### Access:

```
http://IP_VPS
```

---

## 🔁 CI/CD Pipeline (GitHub Actions)

### Trigger:

```bash
git push origin main
```

### Workflow:

1. Build Docker Image
2. Push to Docker Hub
3. SSH to VPS
4. Pull latest image
5. Stop old container
6. Run new container

---

## 🔐 Environment Variables

Create `.env` inside `backend/`:

```env
MONGODB_URL=your-mongodb-url
ACCESS_TOKEN_SECRET=your-secret-key
```

⚠️ Never commit `.env` to GitHub

---

## 🧪 Testing Endpoint (CI/CD Validation)

```
GET /test
```

Response:

```json
{
  "msg": "CI/CD WORKING 🔥"
}
```

---

## 📌 Checkpoints

### ✅ Local Development

* Backend & Frontend running
* MongoDB connected
* API tested

### ✅ Dockerized

* Backend containerized
* Running locally

### ✅ Production Deployment

* VPS running Docker container
* Frontend served via backend
* Nginx reverse proxy working

### ✅ CI/CD Ready

* Auto deploy on push
* Docker Hub integrated
* No manual deployment needed

---

## 🔥 Future Improvements

* HTTPS (Let's Encrypt SSL)
* Custom Domain
* Docker Compose (multi-container)
* Monitoring (Prometheus / Grafana)
* Zero-downtime deployment

---

## 👨‍💻 Author

**IBNU BAYHAQI (DevOps Enthusiast)**

---
