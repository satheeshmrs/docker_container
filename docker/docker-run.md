## docker run redis
 - image take the latest (tag - latest version of tag)

## docker run redis:4.0
- tag
- How do we found the version, using the docker hub

## docker run  (non intractive model)

## docker run -i (interactive mode)
  - application prompt teminal

## docker run -it (interactive mode and terminal attachment)
- application and prompt termina

## docker run
- How docker port listening
- IP of the docker container 172.17.0.2:5000
- Open from a browser access the ip
- outside the docker host -> canot access
- Free port through docker host

## docker run -p 80:5000 kodecloud/webapp
  -P 80: 5000

## Data persistant (mysql)
- var/lib/mysql
- container along with the data will be deleted
- docker run -v /opt/datadir:var/lib/mysql mysql
- implement the external volume
- remain even if we delete

## docker inspect <container-name>
- more details
- n/w information

## docker logs <container-name>
- retrive the log od the container
  
