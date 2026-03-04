# Helm Charts Repository

This repository hosts Helm charts for deploying applications to Kubernetes.

## Architecture

Developer
   │
   ▼
GitHub Repo (Helm Charts)
   │
   ▼
Helm Packaging
   │
   ▼
GitHub Pages (Helm Repository)
   │
   ▼
helm repo add
   │
   ▼
helm install
   │
   ▼
Kubernetes Cluster

## Charts

- backend
- database

## How charts are published

Charts are packaged using:

helm package backend
helm package database

Repository index generated using:

helm repo index .

Charts are published using GitHub Pages.

## How to use the repository

Add Helm repository:

helm repo add myrepo https://sathwikanjali-angelone.github.io/helm-charts-repo

Update repo:

helm repo update

Install applications:

helm install backend myrepo/backend
helm install database myrepo/database
