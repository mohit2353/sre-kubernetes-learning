# Kubernetes Learning Notes

## What is Kubernetes?

Kubernetes is a container orchestration platform.

It helps:
- manage containers
- scale applications
- restart failed containers
- manage deployments automatically

---

# Core Learning Till Now

## 1. Containers

A container is an isolated environment that contains:
- application
- dependencies
- runtime

Example:
- NGINX container
- Go application container

---

## 2. Docker

Docker is used to:
- build containers
- run containers
- manage container lifecycle

### Commands Learned

```bash
docker --version
docker run hello-world
docker ps -a
docker images
docker run -d -p 8080:80 nginx
docker stop <container-id>
```

---

# Docker Concepts

## Image
Blueprint/template.

## Container
Running instance of image.

---

# Kubernetes Basics

## Pod

Pod is the smallest deployable unit in Kubernetes.

Kubernetes runs Pods, and Pods contain containers.

Example:

Pod
 └── Container

---

# Kubernetes Architecture

## Control Plane
Brain of the cluster.

Responsible for:
- scheduling
- cluster management
- API handling

## Worker Node
Runs Pods and containers.

---

# Tools Installed

## kubectl

CLI tool used to communicate with Kubernetes cluster.

### Verify

```bash
kubectl version --client
```

Installed Version:
- v1.35.3

---

# KIND

KIND = Kubernetes IN Docker

Used to create local Kubernetes clusters using Docker.

---

# KIND Installation

```bash
curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.30.0/kind-linux-amd64
chmod +x ./kind
sudo mv ./kind /usr/local/bin/kind
kind version
```

---

# First Kubernetes Cluster

## Create Cluster

```bash
kind create cluster --name my-cluster
```

---

# Cluster Verification

## Cluster Info

```bash
kubectl cluster-info
```

## Nodes

```bash
kubectl get nodes
```

Example Output:

```text
NAME                       STATUS   ROLES           AGE   VERSION
my-cluster-control-plane   Ready    control-plane   71s   v1.34.0
```

---

# Learning Flow

Application
    ↓
Docker Image
    ↓
Container
    ↓
Pod
    ↓
Node
    ↓
Cluster

---

# Current Kubernetes Status

Completed:
- Kubernetes Introduction
- Pod Concepts
- kubectl Setup
- KIND Setup
- First Local Kubernetes Cluster

Next:
- Pods
- Deployments
- YAML
- Logs
- Debugging
