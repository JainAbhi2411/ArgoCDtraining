# 🚀 Argo CD - GitOps Continuous Delivery for Kubernetes  

## 📌 Overview  
Argo CD is a declarative, GitOps-based continuous delivery tool for Kubernetes. It ensures that your application state matches the desired state defined in a Git repository.  

## 🛠️ Installation  

### 1️⃣ Install Argo CD in Kubernetes Cluster  
```sh
kubectl create namespace argocd  
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```
3️⃣ Access the Argo CD UI
```sh
kubectl port-forward svc/argocd-server -n argocd 8080:443  
```

4️⃣ Login to Argo CD

```sh
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d  
```
