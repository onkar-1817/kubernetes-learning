# Kubernetes Learning

This repository contains **Kubernetes** practice manifests, Helm charts, and small example apps that are used to learn core Kubernetes concepts step by step. [web:7][web:3]

## Repository structure

- `Pods/` – Basic Pod YAMLs to understand how containers are scheduled and run on the cluster. [web:3]
- `apache/` – Apache HTTP server Deployment and Service manifests for web server practice.
- `dashboard/` – Resources related to the Kubernetes dashboard or similar UI components.
- `django-todo-app/` – Sample Django todo application deployed on Kubernetes to practice multi-tier apps.
- `helm/` – Helm charts and values files used to deploy some of the example applications. [web:7]
- `mysql/` – MySQL StatefulSet, PersistentVolume, and configuration examples for stateful workloads. [web:3]
- `nginx/` – Nginx Deployment, Service, and (optionally) Ingress examples for reverse proxy.
- `config.yml` – Common configuration or notes used across the examples.
- `meta.txt` – Personal notes, learning plan, or commands related to this repo.

(If any folder is different in your repo, update the description accordingly.)

## Prerequisites

- A running Kubernetes cluster (minikube, kind, k3s, or any managed cluster such as EKS, GKE, AKS). [web:19]
- `kubectl` installed and configured to talk to your cluster. [web:19]
- Optional: `helm` CLI installed for the resources inside the `helm/` directory. [web:16]

## Getting started

1.	Clone this repository:
git clone https://github.com/<your-username>/kubernetes-learning.git
cd kubernetes-learning
2.	Apply a simple example, for example Pods:
kubectl apply -f Pods/
kubectl get pods -A
3. Explore other folders like `nginx/`, `apache/`, `mysql/`, and `django-todo-app/` to see different Kubernetes objects and patterns. [web:3][web:31]

## Learning path using this repo
     Suggested order to practice:
 1. **Pods** – Basics of running containers (`Pods/`).
2. **Deployments & ReplicaSets** – Rolling updates and scaling (`nginx/`, `apache/`).
3. **Services & Ingress** – Exposing applications inside and outside the cluster (`nginx/`, `django-todo-app/`).
4. **ConfigMaps & Secrets** – Externalizing configuration (inside app folders where used).
5. **Persistent Volumes & StatefulSets** – Handling stateful apps (`mysql/`). [web:3]
6. **Helm** – Packaging and reusing configurations (`helm/`). [web:7]

## Notes
This is mainly a personal learning repository, but others who are starting with Kubernetes can also clone it and follow the examples for practice. [web:28]
