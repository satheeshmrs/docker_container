# Kubernetes /K8s:
 - Built by google
 - Container and Orchestration

   -  Developer and Operation will work on together
   - Ops Team can simply deploy the image
   - Containerized application

## Orchestration:
  - Managing container
  - deploying container
  - Kuberenetes is orchestration tool
  - Container orchestration Advantages,
      -  User traffic Load Balanced,
      -  Scalablity,
      -  Ability to do , increament the nodes
      -  Declrative file you can  deploy

## Nodes:
- Node is machine (Worker machine) VM or Physical Machine
- if node fail application is fail
- Need to have more than one Node
- Cluster is Set of nodes together
- SHaring load

## Master:
 - Master is node., Kubernetes installed
 - Montioring other nodes, containers and managing.

## KubeCtl:
 - Command line Tool --> deploying application

## Commands:
 - kubectl get nodes
 - kubectl get nodes -o wide
 - kubectl cluster-info
 - Create a Pod named nginx-pod using the nginx image.
       -  kubectl run nginx-pod --image=nginx

# Pods:
 - Application in the form of container
 - Doesn't deploy directly in nodes
 - POD is encapsulated object of application container (Single instance of applictaion)
 - smallest object is in Kubernetes

   - If you need add additional node,  new instance of pod
   - If current node is not having enough space, you can add pod
   - pod is one-to-one relationship with the container
   - single pod can contain multiple container
   - you might need to connect with other application
   - helper can have it
  
# How to deploy pod:

  - deploy a container with nginx image
  **Kubectl run nginx --image nginx**
      - run the node
   
  - list all the pods
    **kubectl get pods**

 - Which nodes are these pods placed on?
    **kubectl get pods -o wide** 
   


