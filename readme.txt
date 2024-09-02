# Afer the initial deployment AWS deployment via Terraform and Jenkins, run:

# Create databases for prod


# get initial admin password for argcd uni
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d