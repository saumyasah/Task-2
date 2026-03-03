
## 📌 Overview
The project demonstrates expertise in:

- Infrastructure as Code (Terraform)
- Kubernetes orchestration (Azure AKS)
- Microservices deployment
- CI/CD automation (GitHub Actions)
- GitOps deployment (ArgoCD)
- Environment separation (staging & production)
- Security best practices
- Observability-ready architecture
- Production-grade configuration & documentation

---

# 🏗 Architecture Overview

The system is deployed on **Azure Kubernetes Service (AKS)** using Terraform.

## Infrastructure Layer
- Azure Resource Group
- AKS Cluster (node pool)
- Namespaces: `microservices`, `staging`, `production`, `argocd`

## Application Layer
- Frontend (Nginx)
- Backend API (Node.js)
- PostgreSQL (StatefulSet + PVC)
- Horizontal Pod Autoscaler
- Network Policies

## CI/CD Layer
- GitHub Actions (CI)
- Docker image build & push
- Security scanning (Trivy)
- ArgoCD (GitOps CD)
- Automated sync to staging & production

---

# 📂 Repository Structure

Task2/
├── terraform/
├── gitops/
│ ├── argocd-apps/
│ ├── staging/
│ └── production/
├── docs/
└── README.md