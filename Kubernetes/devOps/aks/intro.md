# AKS
- AKS- Azure Kubernetes Services
- AKS is higly available  Secure and fully managed kubernetes Service
- AKS is available on 36 region
- we can deploy any type of workl loads
    - Machine Learning, Windows, Linux or IOT
 
## AKS Architecture:
 - Control Plane
 - Worker Nodes

## Azure AKS Cluster Control Plane:
  - Master Component
    - Container Runtime(Docker)
    - etcd - Key value store (All master and node info)
    - Kube-scheduler (Newly pod, talk through kublet)
    - Kube-apiserver (frontend for control plane) -- everything can talk to this one
    - Kube Control Manager --> Node COntroller, Replication COntroller, Endpoint Controller, SVC point Controler
   
## Node Pools:

  - Container Runtime(Docker)
  - Kublet ->
  - Kube-proxy

## Create AKS:
   - Create Step
       - <img width="1136" height="608" alt="image" src="https://github.com/user-attachments/assets/6ff689d2-8bc3-4523-a89c-d425ed363c96" />
        <img width="1197" height="562" alt="image" src="https://github.com/user-attachments/assets/105c08b3-7cfb-4fde-ac27-eb1da890e5fc" />
        <img width="1281" height="646" alt="image" src="https://github.com/user-attachments/assets/c1e8ecbb-221f-413c-ac97-44aab87415e7" />
        <img width="1677" height="860" alt="image" src="https://github.com/user-attachments/assets/150afd72-2f79-4689-b862-12af496b9373" />
        <img width="1443" height="701" alt="image" src="https://github.com/user-attachments/assets/9c06bbdc-dc43-47d2-b902-707633d75bb3" />

        Connect:
     <img width="1626" height="858" alt="image" src="https://github.com/user-attachments/assets/8a5bb47f-2d7c-4e04-afcb-e949d2044f00" />
     <img width="1501" height="442" alt="image" src="https://github.com/user-attachments/assets/1427ade1-d653-47b2-80b1-86462553f2b7" />

      kubectl version --client=true
     - list down all the nodes
         <img width="1486" height="312" alt="image" src="https://github.com/user-attachments/assets/d71667b3-d8ec-4ca8-a6cf-a6d0171b29c7" />

         <img width="1802" height="592" alt="image" src="https://github.com/user-attachments/assets/5a48dd1b-a259-472a-8ecd-114bc31e75e5" />

```ps
 # Template
az aks get-credentials --resource-group <Resource-Group-Name> --name <Cluster-Name>

# Replace Resource Group & Cluster Name
az aks get-credentials --resource-group aks-rg1 --name aksdemo1

# List Kubernetes Worker Nodes
kubectl get nodes 
kubectl get nodes -o wide
```

```ps
# List Namespaces
kubectl get namespaces
kubectl get ns

# List Pods from all namespaces
kubectl get pods --all-namespaces

# List all k8s objects from Cluster Control plane
kubectl get all --all-namespaces
```


# why K8s:
- Kubernetes is a portable, extensile, open -source platform for managing containerized workloads
- Out oF box features
      - Service discovery and load balancing
      - Storage Orchestration
      - Automated rollouts and rollbacks
      - Automated bin packing
      - Self-healing
      - Secret and Config Management

## Kubernates Fundamental:

### PODS Demo
```ps
# Configure Cluster Creds (kube config) for Azure AKS Clusters
az aks get-credentials --resource-group aks-rg1 --name aksdemo1

# Get Worker Node Status
kubectl get nodes

# Get Worker Node Status with wide option
kubectl get nodes -o wide
```

## Create a Pod
```ps
Create a Pod
# Template
kubectl run <desired-pod-name> --image <Container-Image>
kubectl run nginx --image nginx

# Replace Pod Name, Container Image
kubectl run my-first-pod --image stacksimplify/kubenginx:1.0.0
```

<img width="1583" height="633" alt="image" src="https://github.com/user-attachments/assets/57eacbdc-8f02-468b-953b-3577d65b850f" />


## Describe Pod
  Describe the POD, primarily required during troubleshooting.
  Events shown will be of a great help during troubleshooting.

```ps
# To get list of pod names
kubectl get pods

kubectl describe pods -o wide
# Describe the Pod
kubectl describe pod <Pod-Name>
kubectl describe pod my-first-pod

# Delete pod
kubectl delete pod <Pod-Name>
kubectl delete pod my-first-pod
```

## Services --> to access the application

  - AKS default --> NodePort or Load balancer 






       
 
