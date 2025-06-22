# Kubernetes NGINX Pod Demo

This is a simple demo to show how to use `kubectl` to deploy an NGINX pod to a Kubernetes cluster.

## Prerequisites

- `kubectl` installed and configured
- A running Kubernetes cluster (e.g., Minikube, Kind, or a cloud cluster)

## Steps to Run the Demo

### Step 1: Apply the Pod configuration
kubectl apply -f nginx-pod.yaml

### Step 2: Check the Pod status

kubectl get pods

### Step 3: Port forward to access NGINX

kubectl port-forward pod/nginx-demo 8080:80

Now open your browser and go to:
👉 http://localhost:8080

### Step 4: Clean up

kubectl delete pod nginx-demo
