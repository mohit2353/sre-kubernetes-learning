# Kubernetes Learning Journey 🚀

This repository documents my hands-on Kubernetes learning journey as part of my preparation for an **Intermediate Site Reliability Engineer (SRE)** role.

The goal of this repository is not only to learn Kubernetes concepts but also to understand how they are used in real production environments through practical labs and debugging exercises.

---

## Environment Setup

* Installed Docker on WSL Ubuntu
* Installed `kubectl`
* Installed Kind (Kubernetes in Docker)
* Created a local Kubernetes cluster
* Verified cluster health and connectivity

Commands used:

```bash
kind create cluster --name my-cluster

kubectl cluster-info

kubectl get nodes
```

---

# Topics Completed

## Day 8 – Kubernetes Installation

### Completed

* Installed Docker
* Installed kubectl
* Installed Kind
* Created first Kubernetes cluster
* Verified control plane
* Verified worker node status

### Concepts Learned

* What Kubernetes is
* Why Kubernetes is needed
* Difference between Docker and Kubernetes
* Cluster architecture (Control Plane and Worker Nodes)

---

## Day 9 – Kubernetes Cluster

### Completed

* Connected to Kind cluster
* Explored cluster information
* Verified nodes
* Understood cluster communication

Commands practiced:

```bash
kubectl cluster-info

kubectl get nodes
```

### Concepts Learned

* Kubernetes API Server
* Cluster components
* kubectl communication
* Control Plane overview

---

## Day 10 – Pods

### Completed

* Created first Pod using YAML
* Applied YAML using kubectl
* Verified Pod status
* Understood Pod lifecycle

Commands practiced:

```bash
kubectl apply -f pod.yaml

kubectl get pods

kubectl describe pod nginx-pod

kubectl delete pod nginx-pod
```

### Pod States Learned

* Pending
* ContainerCreating
* Running
* ImagePullBackOff (theory)
* CrashLoopBackOff (introduction)

### Concepts Learned

* Why Kubernetes uses YAML
* Pod specification
* Images
* Containers inside Pods

---

## Day 11 – Labels and Selectors

### Completed

Added labels to Pods.

Example:

```yaml
labels:
  app: nginx
  env: dev
```

Commands practiced:

```bash
kubectl get pods --show-labels

kubectl get pods -l app=nginx

kubectl get pods -l env=dev
```

### Concepts Learned

* Labels
* Selectors
* Filtering Pods
* Organizing workloads

---

## Day 12 – Deployments & ReplicaSets

### Completed

Created first Deployment.

Commands practiced:

```bash
kubectl apply -f deployment.yaml

kubectl get deployments

kubectl get replicasets

kubectl get pods
```

### Concepts Learned

* Deployment
* ReplicaSet
* Desired State
* Current State

### Self-Healing Lab

Deleted one Pod manually.

```bash
kubectl delete pod <pod-name>
```

Observed Kubernetes automatically creating a replacement Pod to maintain the desired number of replicas.

### Learned

* Self-healing
* Desired vs Current state
* Replica management

---

## Day 13 – Scaling Deployments

### Completed

Scaled a Deployment up and down.

Commands practiced:

```bash
kubectl scale deployment nginx-deployment --replicas=5

kubectl scale deployment nginx-deployment --replicas=2
```

### Concepts Learned

* Manual Scaling
* Replica count
* Pod creation
* Pod termination
* Resource optimization

### Introduction to Auto Scaling

Studied the basics of:

* Horizontal Pod Autoscaler (HPA)
* CPU-based scaling
* Minimum and maximum replicas
* Difference between manual scaling and automatic scaling

---

# Kubernetes Concepts Learned

* Kubernetes Architecture
* Control Plane
* Worker Nodes
* Pods
* Labels
* Selectors
* Deployments
* ReplicaSets
* Desired State
* Self-Healing
* Manual Scaling
* Introduction to Horizontal Pod Autoscaler (HPA)

---

# Hands-on Commands Practiced

```bash
kind create cluster

kubectl cluster-info

kubectl get nodes

kubectl apply -f <file>

kubectl get pods

kubectl get deployments

kubectl get replicasets

kubectl describe deployment

kubectl describe pod

kubectl delete pod <pod-name>

kubectl scale deployment <deployment-name> --replicas=<count>

kubectl get pods --show-labels

kubectl get pods -l app=<label>
```

---

# What's Next

The next topics in this learning journey are:

* Services
* ClusterIP
* NodePort
* LoadBalancer
* ConfigMaps
* Secrets
* Volumes
* StatefulSets
* DaemonSets
* Jobs & CronJobs
* Ingress
* RBAC
* Networking
* Production Troubleshooting
* Monitoring & Observability
* GitLab-style SRE Labs

---

## Goal

By the end of this repository, I aim to:

* Build and operate production-like Kubernetes workloads.
* Deploy Go applications on Kubernetes.
* Implement monitoring, autoscaling, and CI/CD.
* Practice real-world troubleshooting scenarios.
* Prepare for Intermediate SRE interviews with confidence.

---

**Status:** 🚧 In Progress
