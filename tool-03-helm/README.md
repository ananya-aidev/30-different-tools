# 🚀 Python FastAPI App with Docker, GitHub Actions & Helm

This is a minimal Python FastAPI web app that is:
- ✅ Dockerized
- ✅ Tested and built via GitHub Actions
- ✅ Deployed using Helm on Kubernetes (like Minikube or EKS)

## 🛠️ Tech Stack
- FastAPI (Python)
- Docker
- GitHub Actions
- Helm
- Kubernetes

## ▶️ Run App Locally
uvicorn app:app --reload --port 5000

## ✅ Run Tests
pytest

## 🐳 Docker
docker build -t your-username/python-app:1.0 .
docker run -p 5000:5000 your-username/python-app:1.0

## 🔁 GitHub Actions CI/CD

GitHub Actions workflow:
- Runs tests
- Builds Docker image
- Pushes to Docker Hub

Required GitHub Secrets:
- DOCKER_USERNAME
- DOCKER_PASSWORD

Workflow path:
.github/workflows/docker-build.yaml

## ⛵ Deploy with Helm on Kubernetes

Start Minikube:
minikube start

Install Helm chart:
helm install python-app ./python-app-chart

Access the app:
minikube service python-app-svc

## 📦 Package Helm Chart
helm package python-app-chart

## 📄 License
MIT License
