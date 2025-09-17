```bash
 docker run -d -p 5000:5000 --restart always --name my-registry registry:2
```

 restart automatically if crash happened
```bash
 curl -X GET localhost:5000/v2/_catalog
```
 check docker registery
 {"repositories":["httpd","nginx"]}
```bash
 docker image prune -a
```
 remove all unused images

 ```bash
docker pull localhost:5000/nginx
```
- pull from local host
 

