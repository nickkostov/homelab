# How to configure the notifiactions in the cluster:

1. Configure the webhook as a secret:

```bash
WEBHOOK="<>"
kubectl -n argocd create secret generic argocd-notifications-secret \
  --from-literal=microsoft-teams-webhook="$WEBHOOK"
```
2. Apply the manifest:

`kubectl apply -f argocd-notifications-cm.yaml

3. 