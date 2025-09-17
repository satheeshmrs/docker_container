## Network

  When you create 3 new network by default
  1. Bridge - default n/w container attached to
  2. none
  3. host

### Bridge
- default n/w container attached to
- docker run ubunt
- private and internal n/w, all container will connected here usually 172.17.0.3
- access any of the container externally, you need to map through port

### HOst
docker run Ubuntu --network=host
- no need to map
- container port can be accessed externally
- you will not able to run multiple container on same port


## none
docker run Ubuntu --network=none
- no n/w, can't be accessed internally or externally
 Isolate the container

## if you want to create multiple internal networks and group the container into different VNET

- we can create the network driver using below command
  ```bash
  docker network create --driver bridge --subnet 182.18.0.0/16 custom-isolated-network
  ```
  - list all n/ws
 ```bash
  docker network ls
 ```

  - inspect the network
  ```bash
  docker inspect custom-isolated-network
  ```

  <img width="1125" height="608" alt="image" src="https://github.com/user-attachments/assets/546743fb-0966-427c-896b-a662ef285cb2" />

  Container can reach using the name

  ## How to access the other container
  - using IP, not ideal
  - using container name is the proper way

 ## Network namespaces
 - create a namespace , virtual ethernet for conatiner


