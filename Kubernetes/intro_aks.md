## Azure Kubernetes Service:

- Kubernetes:
    - Data structures
    - MI/AL

 - Azure Landing Zone:
     - Simple , Repeatable
     - AKS
     - Essential things required for application to run
     - Enterprise security
  
  - AKS Landing Zone

    <img width="921" height="708" alt="image" src="https://github.com/user-attachments/assets/077afca1-3287-4151-90b6-b012630b22a2" />

    - to connect other services in predictable manner
   
## AKS:
az account show
- Show the current account details

az configure --defaults group=RG1-KodeKloud-AKS
az aks get-credentials --name aks-kodecloud-app
kubectl config current-context
kubectl get nodes
kubectl get deployment
kubectl get pods
kubectl create deployment kodcloudapp --image=hprnamc --replicas=1

kubectl expose deployment kodecloudapp --type=LoadBalancer --port=80 --target-port=80

kubectl get service

<img width="705" height="117" alt="image" src="https://github.com/user-attachments/assets/7fcd693a-4e82-4c78-9f44-8ad2f74e9f78" />

## Scale the application
kubectl scale deployment kodekloudapp --replicas=5
<img width="1042" height="833" alt="image" src="https://github.com/user-attachments/assets/56e49f01-60b4-4849-bb37-53a25e983823" />


## Important to Learn

  - Nodes
  - Pods
  - Services
  - Deployment

## KubeCtl with Field-selector
kubectl get pods --field-selector=status.phase=Running
- filter running pods

  <img width="1372" height="556" alt="image" src="https://github.com/user-attachments/assets/a36e56c5-b4f2-4399-94b5-7c2c2799b5fb" />


  <img width="922" height="150" alt="image" src="https://github.com/user-attachments/assets/6fa13198-490c-4b06-947e-caf3c90bce4e" />

  <img width="1460" height="770" alt="image" src="https://github.com/user-attachments/assets/d7c4a096-456d-40c9-95c5-0de17c6cffc1" />




    





