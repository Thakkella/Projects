# Voting Application

**Project link: https://github.com/Thakkella/example-voting-app-project**

**Reference links:**
**https://argo-cd.readthedocs.io/en/stable/getting_started/**

**https://kubernetes.io/docs/tasks/configure-pod-container/pull-image-private-registry/**

**https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/linux-agent?view=azure-devops&tabs=IP-V4**

## Imported the repository from GitHub

![alt text](<Screenshot 2026-10-20 141012.png>)

## Created a private Azure Container Registry (ACR)

![alt text](<Screenshot 2026-10-20 144723.png>)

## Created a VM in Azure for self-hosted agent
## You'll need a Personal Access Token (PAT) to register the agent in Azure DevOps

![alt text](<Screenshot 2026-10-20 164743.png>)
![alt text](<Screenshot 2026-10-20 171020.png>)
![alt text](<Screenshot 2026-10-20 171810.png>)

## Created pipeline in Azure DevOps for the Result microservice and ran pipeline

![alt text](<Screenshot 2026-10-20 171940.png>)
![alt text](<Screenshot 2026-10-20 172040.png>)
![alt text](<Screenshot 2026-10-20 172525.png>)

## Similarly created the pipelines for Vote and Worker microservice and ran them

![alt text](<Screenshot 2026-10-20 191741.png>)

## Verified the repositories are created in ACR and images are pushed with the latest tags

![alt text](<Screenshot 2026-10-20 193049.png>)

## Created Azure Kubernetes (AKS) cluster

![alt text](<Screenshot 2026-10-20 210955.png>)

## Followed the reference link to install and configure ArgoCD on the AKS cluster for GitOps

![alt text](<Screenshot 2026-10-20 211244.png>)

## We need to retrieve the initial login admin password from the ArgoCD secret

![alt text](<Screenshot 2026-10-20 211537.png>)

## Changed the ArgoCD server service type to NodePort to login using the Node IP

![alt text](<Screenshot 2026-10-20 212139.png>)

## Allowed Inbound connection on the AKS cluster to login ArgoCD

![alt text](<Screenshot 2026-10-20 212836.png>)

## Created a PAT in Azure DevOps for the ArgoCD to connect to the repository

![alt text](<Screenshot 2026-10-20 213618.png>)
![alt text](<Screenshot 2026-10-20 214042.png>)
![alt text](<Screenshot 2026-10-20 214132.png>)

## Created Application and verified the Health and Sync status

![alt text](<Screenshot 2026-10-20 214908.png>)
![alt text](<Screenshot 2026-10-20 215123.png>)

## Created shell script to update the Kubernetes deployment manifests files with the latest tag

![alt text](<Screenshot 2026-10-20 221401.png>)

## Added the Update stage in the pipeline to automatically update when the pipeline is triggered

![alt text](<Screenshot 2026-10-20 221954.png>)
![alt text](<Screenshot 2026-10-20 222602.png>)

## Enabled Admin user for the ACR to create a secret in AKS cluster, using imagePullSecrets Kubernetes can pull container images from a private container registry

![alt text](<Screenshot 2026-10-21 180535.png>)
![alt text](<Screenshot 2026-10-21 182142.png>)

## Whenever any code change is made the pipeline will be triggered, latest image is pushed to the ACR repository 

![alt text](<Screenshot 2026-10-21 182452.png>)
![alt text](<Screenshot 2026-10-21 184452.png>)
![alt text](<Screenshot 2026-10-21 184553.png>)

## ArgoCD will watch for the changes in the Kubernetes manifests files and deploy latest version onto the cluster

![alt text](<Screenshot 2026-10-21 184754.png>)
![alt text](<Screenshot 2026-10-21 190402.png>)

## Make sure to allow the required inbound connections to the cluster for the result and vote services

![alt text](<Screenshot 2026-10-21 190428.png>)

## Finally verify the application by accessing both the vote and result microservices

![alt text](<Screenshot 2026-10-21 201800.png>)
![alt text](<Screenshot 2026-10-21 202053.png>)