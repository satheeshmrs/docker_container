## Docker container from ubuntu images
docker run ubuntu
- it will be stopped
- container not to host os
- container host app server, web app, db,
- once the task is completed it will exist
- Container only live if the application breaks
- who define what process run
- NGINX
- CMD "nginx"
- CMD "bash"
- it cannot find the terminal it breaks

docker run ubuntu sleep 5

FROM Ubuntu
CMD sleep 5

## JSON FORMAT
CMD ["sleep","param1"]
CMD ["sleep", "5"]

## Param --> entry point
ENTRYPOINT ["sleep"]
docker run ubuntu-sleeper 10
- sleep 10 seconds

## Command entry point
ENTRYPOINT
