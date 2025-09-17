# Docker Engine and Architecture
- Simply referred host
  <img width="522" height="382" alt="image" src="https://github.com/user-attachments/assets/7c1f3c0d-bc68-41bf-b4da-38c782829709" />
  -Deamon:
   - backgroud process
  - Deamon:
      - managing all images and containers
  - CLI : Performing (Rest api to interact with Deamon")
  - Remote Docker engine
 
    ## Containerization:
    <img width="1327" height="722" alt="image" src="https://github.com/user-attachments/assets/3bff8b8f-e64e-4e7f-9aab-f9b9f1840de6" />
    - name spaces to processid, interprocess communication
    - Namespace -PID:
    - Linux process starts root process trigger other process
    - two process cannot have same id
    - Child system container (PID: 1) --> Namespace id
    - Process id --> different process id when if it is run in the container

    ## NameSpace:

    ## Resources:
      - Host
      - Resources
      - How much allocated.
      - Conatiner can use all memory and cpu
      - we can restrict using "cgroups"
      - docker run --cpus=.5 ubuntu
      - docker run --memory=100m ubuntu
   
    

    
    
    
       
      
     
      

