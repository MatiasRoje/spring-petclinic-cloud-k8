# Spring PetClinic Kubernetes Manifests

This repository contains the Kubernetes manifests used to deploy the Spring PetClinic microservices application on an AWS EKS cluster.
The manifests are automatically updated through our CI pipeline from the main repository.

## Repository Structure
- **Helm Charts**: Manages the application’s microservices deployment.
- **Variables files**: Environment-specific configurations for `staging`, and `prod`.

## CI/CD Integration
- Jenkins CI pipeline in the primary repository automatically updates image tags in this repository.
- ArgoCD is connected via a webhook and listens for changes in this repository, triggering automatic deployments to the Kubernetes cluster.

## Environments
- **Staging**: Automatically deployed after CI completes.
- **Production**: Requires manual approval for deployment.
