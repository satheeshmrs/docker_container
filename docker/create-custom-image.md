# Sample Steps
- 1. OS -ubuntu
  2. Update apt repo
  3. install dependancies using apt
  4. install python dependancies using pip
  5. copy source code to /opt folder
  6. Run the web server using "flask" command
 
  ## Create a file Dockerfile (dockerfile)
  ```bash
  FROM ubunt
  RUN apt-get update
  RUN apt-get install python
  RUN pip install flask
  RUN pip install flask-mysql
  COPY ./opt/source-code
  ENTRYPOIN FLASK_APP=/opt/source-code/app.py
  ```

  ## docker build Dockerfile -t satheesh/my-custom-app
  ## docker push satheesh/my-custom-app
   - pushing to dockerfile
 
  ## Docker registery

  ## DOckerfile
  <INSTRUCTION> <argument?
  - Instruction in CAPITAL LETTER
  - Arguments in the small
  - All custom docker image from the file
  - COPY to copy from local to docker image
  - ENTRYPOINT, command to run when the container run
  - Each command (instruction by layers) - each layers will be having previous state changes
  - if you run Docker history <image-name> you can track the state
 
  ## Failure
  - Step 3 fail --> previous layer from the cache and continue from the step 2
  - Only below the layer rebuild
 
  ## What to contanierize
  - we can containerize everything
 
  ## DEMO:
  ``` bash
  FROM python:3.6

RUN pip install flask

COPY . /opt/

EXPOSE 8080

WORKDIR /opt

ENTRYPOINT ["python", "app.py"]
```

Build a docker image using the Dockerfile and name it webapp-color. No tag to be specified.

docker build -t webapp-color ./webapp-color

  
    
  
  
