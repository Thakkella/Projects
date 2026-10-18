# AKS Cluster Demo

## Deploying sample application to AKS Cluster

**Project link: https://github.com/Thakkella/kodekloud-aks**

## Deployed application to AKS cluster and exposed the service type to Load balancer

![alt text](<Screenshot 2026-10-10 182541.png>)
![alt text](<Screenshot 2026-10-10 182306.png>)
![alt text](<Screenshot 2026-10-10 181931.png>)
![alt text](<Screenshot 2026-10-10 182001.png>)

## Scaling the Deployment using kubectl

![alt text](<Screenshot 2026-10-10 183922.png>)
![alt text](<Screenshot 2026-10-10 183709.png>)

## Scaling the Nodes using Azure CLI

![alt text](<Screenshot 2026-10-10 185446.png>)

## Upgraded application from v1 to v2 version

![alt text](<Screenshot 2026-10-10 193636.png>)
![alt text](<Screenshot 2026-10-10 193852.png>)
![alt text](<Screenshot 2026-10-10 194326.png>)

## Tested the Roll Back to a Previous Revision

![alt text](<Screenshot 2026-10-10 195141.png>)
![alt text](<Screenshot 2026-10-10 195242.png>)

# Testing the traffic flow with Open Service Mesh (OSM)

## Created 3 namespaces to test the traffic

![alt text](<Screenshot 2026-10-11 184333.png>)
![alt text](<Screenshot 2026-10-11 184443.png>)

## Deploy the application and port-forward to verify the default traffic

![alt text](<Screenshot 2026-10-11 185531.png>)
![alt text](<Screenshot 2026-10-11 185625.png>)

## Disabled the permissive traffic policy to verify whether the traffic is stopped

![alt text](<Screenshot 2026-10-11 190108.png>)
![alt text](<Screenshot 2026-10-11 190234.png>)
![alt text](<Screenshot 2026-10-11 190448.png>)

## Applied the explicit allow traffic and can see the traffic is resumed

![alt text](<Screenshot 2026-10-11 190939.png>)
![alt text](<Screenshot 2026-10-11 191003.png>)

## Applied the traffic splitting based on weight

![alt text](<Screenshot 2026-10-11 192015.png>)
![alt text](<Screenshot 2026-10-11 192033.png>)

## Updated the weight to 100 to pass the traffic only from v2

![alt text](<Screenshot 2026-10-11 192313.png>)
![alt text](<Screenshot 2026-10-11 192335.png>)

## Similarly we can enable Azure Policy for governance and compliance

![alt text](<Screenshot 2026-10-11 213827.png>)
![alt text](<Screenshot 2026-10-11 214032.png>)