## Check version of Kubernetes Cluster:
kubectl version --short
<img width="1047" height="122" alt="image" src="https://github.com/user-attachments/assets/206de982-fd45-47e2-87af-4e77f9da5ee1" />

## Create Deployment (deploy the cluster)
kubectl create deployment kodecloudapp --image=kodecloudapp:v1 --replica=2

## Deploy the app
kubectl get deploy

## Mapping Port 
kubectl expose deployment kodecloudapp --type=LoadBalancer --port=8080 --target-port=80

exposed.

-- We don't know which replica is serving
-- application code to change.

