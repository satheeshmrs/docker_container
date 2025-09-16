# Find the config value
docker inspect <image-name>
- under config section you can find the env variables

## Set envinronment variable
docker run -d \
  --name blue-app \
  -e APP_COLOR=blue \
  -p 38282:8080 \
  kodekloud/simple-webapp

  docker exec -it blue-app env

  docker run --name mysql-db -e MYSQL_ROOT_PASSWORD=db_pass123 -d mysql
  
