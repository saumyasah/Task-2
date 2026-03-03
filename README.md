# 🚀 FastAPI CI/CD Deployment on Azure AKS

This project demonstrates a complete end-to-end DevOps pipeline:

- FastAPI application
- Docker containerization
- GitHub Actions CI/CD
- Trivy security scanning
- Azure Container Registry (ACR)
- Azure Kubernetes Service (AKS)
- Helm deployment

---

## 🏗️ Architecture

Developer → GitHub → GitHub Actions → Docker Build → Trivy Scan → Push to ACR → Deploy to AKS via Helm

---

## 📁 Project Structure

```
Task-2/
│
├── app/                  # FastAPI application
│   ├── main.py
│   ├── test_app.py
│   ├── requirements.txt
│   └── Dockerfile
│
├── k8s/                  # Helm chart for AKS
│   ├── Chart.yaml
│   ├── values.yaml
│   └── templates/
│       ├── deployment.yaml
│       └── service.yaml
│
└── .github/workflows/
    └── ci-cd.yaml        # CI/CD Pipeline
```

---

## ⚙️ CI/CD Pipeline Stages

### 1️⃣ Lint
flake8 checks code formatting.

### 2️⃣ Unit Tests
pytest runs FastAPI test cases.

### 3️⃣ Docker Build
Application is containerized.

### 4️⃣ Security Scan
Trivy scans for vulnerabilities (HIGH & CRITICAL).

### 5️⃣ Push to Azure Container Registry

### 6️⃣ Deploy to AKS
Helm installs/updates Kubernetes deployment.

---

## 🐳 Docker Build (Local)

```bash
docker build -t myapp .
docker run -p 8000:8000 myapp
```

Visit:
```
http://localhost:8000
```

---

## ☁️ Azure Deployment

Login:
```bash
az login
```

Get AKS credentials:
```bash
az aks get-credentials --name dodo-aks --resource-group dodo-devops-rg
```

Check service:
```bash
kubectl get svc
```

---

## 🔐 Security Scanning

Trivy blocks the pipeline if HIGH or CRITICAL vulnerabilities are detected.

---

## 📸 Screenshots

(See screenshots section below)

---

## 🧠 Technologies Used

- FastAPI
- Docker
- GitHub Actions
- Azure CLI
- Azure AKS
- Azure ACR
- Helm
- Trivy

---

## 🎯 Outcome

This project demonstrates production-ready CI/CD with secure container deployment to Azure Kubernetes Service.

---

## 👩‍💻 Author

Saumya Sah