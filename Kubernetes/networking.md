## Networking Options

## Network Security:
- VNET:
-   One or more IP address intent to use it
-   CIDR ( IP address management)
-   SImple n/w address or mask to mention range
-   Ip/4 or IP/6
-   Need to mention subnet
-   Subnet is subset of virtual networks

NSG:
 - UDR
 - Filter routes
 - INbound or Outbound traffic
 - UDR --> Talk to another POD
 - Route table where to forward packets
 - UDR
 - PGPR
 - Subnet --
 - Frontend to subnet -->

AKS n/w:
- kUbe Net
    - Plugin will deployed
  - Nodes get an IP
  - PODs recived from
  - NAT PODs can recive traffic
  - PODS can communicate each other in same Nodes
  - Other Node communicate through UDR
  - POD1 --> POD2 (UDR)
  - Outside of cluster --> SNET
  - SourceNetwork --> another Vnet VM ip --> SNAT source Ip
 
CNI:
  - VM get IPs
  - Get PODs will get IP
  - Directly routable from IP
  - Seemless connectivity
  - PODS can connect any n/w or external services
  - Better n/w
  - Implementatio of container n.w interface that is inline CNCF (Cloud n/w foundation)

  CNC
  --> Networking
  --> IP Address Management
  --> IP0, IP1, --> IP1, IP2
  --> CLI --> How many pods want to deploy
  --> pool ip is assigned
  --> VNET bridge
  --> 250 Containers/POD/VM
  --> 64000IP

  <img width="1390" height="743" alt="image" src="https://github.com/user-attachments/assets/bbbb16c1-f1b6-4b24-89ed-100c5a4617f6" />

 <img width="1402" height="556" alt="image" src="https://github.com/user-attachments/assets/e81955ae-744a-431a-a610-72ea5cecd8ab" />


<img width="1377" height="660" alt="image" src="https://github.com/user-attachments/assets/1a52397e-7ac7-4e7d-b40e-3aefd680d5c0" />

N/W Policies:
  - NSG
      --> PODs will go and expire soon
      --> another ip
      --> rules based --> pod label secure
  - Policies:
      --> Specification to define, yaml --> policies around
      --> n/w policies
      --> Namespaces
      --> every node and sit in the policy
      --> Policy ingen
      --> Ip table rules
      --> HNS (Windows kernal)
      --> In the IP tables
      --> Linux bridge functionality
    <img width="1375" height="792" alt="image" src="https://github.com/user-attachments/assets/746d4092-4417-44ef-bec6-270c279d83ec" />
     --> Calico policies
    

  
