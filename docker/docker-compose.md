## Docker compose yaml
- if you want to setup complex application with multiple services
- docker-compose.yml file
- sample docker-compose yaml
  ```yaml
  services:
     web:
      image:"satheesh/sample-app"
     database:
      image:"mongodb"
     messaging:
      image:"redis:alpine"
     orchestration:
      image: "ansible"
  ```

  ## docker-compose up:
  - command to run the docker file.
 
  ## communicate two containers in docker using
  -link command
  ```bash
  docker run -d --name=redis redis
  ```
  - this will run the redis conatiner and to link this container into a new container
  use --link param
  ```bash
  docker run -d --name=vote -p 5000:80 --link redis:redis voting-app
  ```
  - --link <link-name>:<container-name>
  - create a entry /etc host file into voting-app and
 
  ## two link
  ```bash
  docker run -d --name=vote -p 5000:80 --link db:db --link redis:redis voting-app
  ```

  ## docker-compose
  ```yaml
  redis: #Name of the container
    image: redis #name of the image
  db:
    image: postgres:9.4
  vote:
    image: voting-app
    ports:
      -5000:80
    links:
      - redis

  result:
    image: result-app
    ports:
      - 5001:80
    links:
      - redis
      - db:db 
  worker:
    image: worker
  ```
  ** run Docker-compose up command

  ## if you want to build the docker file along with the compose

   ```yaml
  redis: #Name of the container
    image: redis #name of the image
  db:
    image: postgres:9.4
  vote:
    build: ./vote # folder name where the dockerfile is located.
    ports:
      -5000:80
    links:
      - redis

  result:
    image: result-app
    ports:
      - 5001:80
    links:
      - redis
      - db:db 
  worker:
    image: worker
  ```
  
