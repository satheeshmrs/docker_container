# Docker Command

  ## docker Run:
    - Run the container from a docker image
    - docker run nginx
    - if the image is not available it will pull the images from dockerhub, only on first time

  ## docker ps:
    - List down all the containers active in the system
    - Docker ps -a
    
  ## Docker stop <Container_name>
    - Stop the container

  ## Docker Ps -a
    - Previously dead/"not-active also
    
  ## Docker rm <container-name>
    - Remove the container

  ## docker images
  - List of all images

  ## docker rmi <image-name>
  - Remove all the container before the image
  - remove all the images

  ## docker Pull <image-name>
    - only pull the image from dockerhub

  ## docker run ubuntu
   - Immediately stop
   - bc

  ## docker run ubuntu sleep 5

  ## docker exec <container-name> cat /etc/hosts

  ## docker run -d kodecloud/webapp
  - run the container in the backgroud

  ## docker attach a043d

  ## docker rm $(docker ps -a -q)
  - Remove all container active and non-active

  ## docker run -d --name webapp nginx:1.14-alpine
  - Run a container with the nginx:1.14-alpine image and name it webapp

 ## docker rmi -f $(docker images -q)
 - Delete all images on the host
  
  
    
    
