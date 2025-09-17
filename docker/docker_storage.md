## Docker Advanced concept
### Docker Storage
    - FileSystem (Folder structure):
      /var/lib/docker
      ├── aufs
      ├── images
      └── containers 
      └── volumes

  ### Layered architecture
    - base ubuntu system
    - changes in apt packages
    - changes in pip changes
    - source code
    - update entry point
    - Docker caches the layer
    and it will use it for other images and also for update docker
    - it will save time --> for rebuild and create
    - Life of the layer is only the container is active
    Conatiner layer --> Read/write
    Image Layer --> Read only
    Container --> you can change the app.py only on one container
              --> Container file can be read/write
              --> container is exited, all will be removed
    --> I wish to modify the app file, does't mean can't modify.. you can modify and different version in the write layer (COPY-ON-WRITE)
    --> Get rid of the container, the file will be removed
    --> if we want to persist the data

  ## Docker volume:
    docker volume create data_volume

    --> when you are creating the container
    docker run -v data_volume:/var/lib/mysql mysql

    --> what if not creating volume before container., docker will create the volume

    --> data is located in another place
      docker run -v data_volume /data/mysql:/var/mysql my sql
    --> from any location

    Using -V is old version

    docker run --mount type=bind, source=/data/sql, target=/var/lib/mysql

  ## Storage drivers
    --> AUFS
    --> ZFS
    --> Device Mapper
    --> Overlay
    --> Overlay2
