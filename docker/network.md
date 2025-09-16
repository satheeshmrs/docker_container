## Networking
- front-end - front end traffic
- back-end - back end traffic
  ```yaml
  version: 2
  services:
    redis:
      image: redis
      networks:
        - back-end
    db:
      image: postgres: 9.6
      networks:
        - back-end
    vote:
      image: voting-app
      networks:
        - front-end
        - back-end
    result:
      image: result
      networks:
        - front-end
        - back-end
    networks:
        - front-end
        - back-end
  ```
    - segregating the front and backend network
 
   ```yaml
  version: 3
  services:
    redis:
      image: redis
      networks:
        - back-end
    db:
      image: postgres: 9.6
      environment:
         POSTGRES_USER: postgres
         POSTGRES_PWD: postgres
      networks:
        - back-end
    vote:
      image: voting-app
      networks:
        - front-end
        - back-end
    result:
      image: result
      networks:
        - front-end
        - back-end
    networks:
        - front-end
        - back-end
  ```
