
# 🚀 Flask App Deployment with Docker

This repository contains a simple **Flask web application** containerized using Docker.
It includes both:

* `Dockerfile` (Single-stage build)
* `Dockerfile.multistage` (Multi-stage optimized build)

The project demonstrates how to containerize and deploy a Flask application using Docker best practices.

---

## 📌 Project Overview

* 🐍 Backend: Flask (Python)
* 🐳 Containerization: Docker
* ⚡ Optimized Image: Multi-stage Docker build
* 🌐 Exposed Port: 5000 (Default Flask port)

---

## 📂 Project Structure

```
.
├── app.py
├── run.py
├── requirements.txt
├── Dockerfile
├── Dockerfile.multistage
├── templates/
│   └── index.html
└── README.md
```

---

## 🐳 Dockerfile (Single Stage)

The `Dockerfile` builds the Flask app in a single stage.

### 🔹 Build Image

```bash
docker build -t python-app .
```

### 🔹 Run Container

```bash
docker run -d -p 5000:5000 --name flask-container python-app
```

Open in browser:

```
http://localhost:5000
```

---

## 🐳 Dockerfile.multistage (Multi-Stage Build)

The `Dockerfile.multistage` uses multi-stage build to:

* Reduce image size
* Improve security
* Remove unnecessary build dependencies
* Follow production best practices

### 🔹 Build Multi-stage Image

```bash
docker build -f Dockerfile.multistage -t flask-app-multistage .
```

### 🔹 Run Container

```bash
docker run -d -p 5000:5000 --name flask-container-ms flask-app-multistage
```

---

## 🛠 Technologies Used

* Python
* Flask
* Docker
* HTML (Jinja Templates)

---

## 📦 Requirements

Make sure Docker is installed:

```bash
docker --version
```

---

## 🎯 Key Learning Objectives

This project demonstrates:

* How to containerize a Flask application
* Difference between single-stage and multi-stage Docker builds
* Optimizing Docker image size
* Running containers and mapping ports
* Basic deployment workflow

---

## 🚀 Future Improvements

* Add Docker Compose
* Deploy on AWS / EC2
* Add Nginx reverse proxy
* Add CI/CD pipeline (GitHub Actions / Jenkins)

---

## 👨‍💻 Author

**Adnan Khan**
CSE Student | DevOps & Cloud Enthusiast
Learning Docker, AWS, Kubernetes & CI/CD 🚀

---

