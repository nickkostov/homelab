#### Install ArgoCD

kubectl create namespace argocd

kubectl apply -n argocd \
  -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

#### Get inital Access password:

```bash
kubectl -n argocd get secret argocd-initial-admin-secret \
  -o jsonpath="{.data.password}" | base64 -d && echo
```
- Install Argocd CLI and Change Password:

```
argocd login 192.168.2.210/domain --username admin --password <current-password> --insecure
argocd account update-password
```

User is admin :D