# ARGO-APP
- **This Repo contains the Kubernetes manifest files for the Web Application.**
- **The Pipeline of EKS-APP Repo updates the image tag in Deployment file.**
- **ArgoCD Application is configured to Monitor this Repo. When the image tag gets updated the ArgoCD applications picksup the change and then deploys it to the cluster.**
- **gitignore folder contains the ArgoCD Application file**
  
---

# Argo CD Application: web-app

This Argo CD Application manifest deploys a Kubernetes application from a Git repository to a specified namespace.

## Overview

- **Name:** web-app
- **Namespace:** argocd

## Specifications

### Source

- **Repository URL:** [https://github.com/Vizzwastaken/ARGO-APP.git](https://github.com/Vizzwastaken/ARGO-APP.git)
- **Path:** `.`
- **Target Revision:** `main`

### Destination

- **Server:** `https://kubernetes.default.svc`
- **Namespace:** `web-app`

## Prerequisites

Before deploying this application using Argo CD, ensure:

1. **Argo CD Installation:** Argo CD is installed and accessible in your Kubernetes cluster.
2. **Git Repository Access:** Ensure the specified Git repository is accessible by Argo CD.
3. **Kubernetes Cluster:** Access to the Kubernetes cluster where you want to deploy the application (`https://kubernetes.default.svc`).

## Deployment Instructions

1. **Login to Argo CD UI or CLI:**
   
   Use the Argo CD UI or CLI to login and access the Argo CD dashboard.

2. **Create Application:**
   
   - Navigate to the Argo CD UI or use CLI to create the application.
   - Use the following YAML manifest or equivalent CLI command to create the application:
   
     ```bash
     kubectl apply -f argo-application.yaml
     ```
   
   Replace `argo-application.yaml` with the filename containing the above manifest.

3. **Monitor Deployment:**
   
   Once the application is deployed, monitor the deployment status using Argo CD UI or CLI.


## Troubleshooting

- **Access Issues:** Verify access to the Git repository and Kubernetes cluster.
- **Deployment Failures:** Check Argo CD logs and Kubernetes events for any errors.
- **Sync Issues:** Ensure Argo CD can sync with the repository and Kubernetes cluster.


---
