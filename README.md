## external secret operator installation

```
helm repo add external-secrets https://charts.external-secrets.io
```

Update Helm repositories

```
helm repo update
```

Install External Secrets Operator

```
helm install external-secrets external-secrets/external-secrets \
  --namespace external-secrets \
  --create-namespace \
  --version 0.20.4
```

connection from external secret to vault with token

```
kubectl create secret generic vault-token --from-literal=token=root
```
