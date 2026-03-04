
# Helm Charts Repository

This repository hosts Helm charts used to deploy applications into a Kubernetes cluster.

---

# Repository Structure

```
helm-charts-repo
├── backend/                # Helm chart for backend application
├── database/               # Helm chart for database
├── backend-0.1.0.tgz       # Packaged backend chart
├── database-0.1.0.tgz      # Packaged database chart
├── index.yaml              # Helm repository index
└── .github/workflows       # GitHub Actions workflow
```

---

# Architecture

```
Developer
   │
   ▼
GitHub Repository
(helm-charts-repo)
   │
   ▼
Helm Chart Packaging
helm package backend
helm package database
   │
   ▼
GitHub Pages
(Helm Chart Repository)
   │
   ▼
helm repo add
   │
   ▼
helm install
   │
   ▼
Kubernetes Cluster
```

---

# Helm Repository URL

```
https://sathwikanjali-angelone.github.io/helm-charts-repo
```

---

# How to Use the Helm Charts

## 1 Add the Helm repository

```
helm repo add myrepo https://sathwikanjali-angelone.github.io/helm-charts-repo
```

---

## 2 Update Helm repositories

```
helm repo update
```

---

## 3 Search charts

```
helm search repo myrepo
```

---

## 4 Install backend

```
helm install backend myrepo/backend
```

---

## 5 Install database

```
helm install database myrepo/database
```

---

# Verify Deployment

Check deployed releases

```
helm list
```

Check running pods

```
kubectl get pods
```

Example output

```
backend-xxxxx   Running
database-xxxxx  Running
```

---

# Summary

This repository provides:

• Helm charts for backend and database
• Packaged Helm charts
• Helm repository hosted using GitHub Pages
• Kubernetes deployments using Helm
