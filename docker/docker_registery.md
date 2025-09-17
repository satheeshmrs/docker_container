## Registery
- it's a repository
- image name nginx --> repository name or /library/nginx
- library --> standard one and
- since we are not mentioned, docker hub or docker.io
- gcr.io
- publically accessible
- you can internally host

  ## Private registeray
  - ACR
  - choose to make private
  - only accessible
  - you need to login
  - docker login command
    ```bash
    docker login private-resgitery.io
    ```
## docker registery
 - Custom image is available
 - you can run the container
 - using tag you cann create

   ```bash
   docker run -d -p 5000:5000 --name registery registry: 2
   docker image tag my-image localhost:5000/myimage
   docker push localhost:5000/my-image
   ```
   - pull image from local host and access the image
   
