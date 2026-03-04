Helm Charts Repository
This repository hosts Helm charts for deploying applications to Kubernetes.
Repository Structure
helm-charts-repo
├── backend/              # Helm chart for backend service
├── database/             # Helm chart for database service
├── backend-0.1.0.tgz     # Packaged backend Helm chart
├── database-0.1.0.tgz    # Packaged database Helm chart
├── index.yaml            # Helm repository index
└── .github/workflows     # GitHub Actions workflow

Architecture
Developer
   │
   ▼
GitHub Repository (helm-charts-repo)
   │
   │ Helm Charts
   ▼
Helm Packaging
(helm package)
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

Workflow
1. Store Helm Charts
Helm charts are stored inside this repository.
Example:
backend/
database/

2. Package Helm Charts
Charts are packaged using Helm.
helm package backend
helm package database
This generates:
backend-0.1.0.tgz
database-0.1.0.tgz

3. Create Helm Repository Index
helm repo index .
This generates:
index.yaml

4. Publish Helm Repository
The repository is published using GitHub Pages.
Helm repository URL:
https://sathwikanjali-angelone.github.io/helm-charts-repo

5. Use Helm Charts for Deployment
Add Helm repository:
helm repo add myrepo https://sathwikanjali-angelone.github.io/helm-charts-repo
Update repo:
helm repo update
Install applications:
helm install backend myrepo/backend
helm install database myrepo/database
Upgrade deployments:
helm upgrade backend myrepo/backend
helm upgrade database myrepo/database

Kubernetes Deployment
After installation the applications run inside the Kubernetes cluster.
Check running pods:
kubectl get pods
Example output:
backend-pod    Running
database-pod   Running

Summary
This repository provides:
* Helm charts for applications
* Packaged charts
* Helm repository using GitHub Pages
* Deployment to Kubernetes using Helm
