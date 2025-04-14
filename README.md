# SIT323/SIT737 - Cloud Native Application Development
## Creating a Kubernetes Cluster for a Containerized Application

This repository contains the necessary files and instructions to deploy a containerized app.js application to a Kubernetes cluster. It was created as part of the SIT323/SIT737 Cloud Native Application Development unit.

## Prerequisites

Before getting started, ensure you have the following tools installed:

- Git
- Visual Studio Code (or any code editor)
- Node.js
- Docker
- Kubernetes (minikube for local development)
- Kubernetes CLI (kubectl)
- Docker CLI

## Step-by-Step Guide

### 1. Setup the Kubernetes Cluster

### 2. Create the Docker Image

docker build -t node-kubernetes-app:v1 .

### 3. Deploy to Kubernetes

kubectl apply -f deployment.yaml

# Check deployment status
kubectl get deployments
kubectl get pods

# Create the service
kubectl apply -f service.yaml

# Check the service status
kubectl get services

### 4. Access the Application

You can now access the application at http://localhost:3000.

### 5. Interacting with the Kubernetes Deployment

kubectl scale deployment node-kubernetes-app --replicas=5

# Check logs from a pod
kubectl logs -l app=nodejs-app

# Get detailed information about a pod
kubectl describe pod <pod-name>
