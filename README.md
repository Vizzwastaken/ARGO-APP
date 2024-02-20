# ARGO-APP
- **This Repo contains the Kubernetes manifest files for the Web Application.**
- **The Pipeline of EKS-APP Repo updates the image tag in Deployment file.**
- **ArgoCD Application is configured to Monitor this Repo. When the image tag gets updated the ArgoCD applications picksup the change and then deploys it to the cluster.**
- **gitignore folder contains the ArgoCD Application file**
  
