# Day 10 - First Pod

Created first nginx Pod using YAML.

Commands Used:

kubectl apply -f pod.yaml
kubectl get pods
kubectl describe pod nginx-pod
kubectl logs nginx-pod

Learnings:
- Pod is the smallest deployable unit in Kubernetes.
- Kubernetes schedules Pods, not containers.
- ContainerCreating means Kubernetes is preparing the container.
- Running means container is healthy and operational.
