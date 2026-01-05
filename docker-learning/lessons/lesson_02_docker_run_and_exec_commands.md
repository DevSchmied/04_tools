## Block 1. Docker `run` Command and Basic Docker Commands

### Tasks

1. Find available container images with the name **nginx** in the public Docker repository.
2. Display a list of local Docker images.
3. Download the **nginx** image to the local machine.
4. Run a container from the **nginx** image in detached mode with port mapping **8123:80**.
5. Display a list of running containers.
6. Stop a container by specifying its name.
7. Stop a container by specifying its identifier (ID).
8. Check the correctness of the **Nginx** web server configuration files.
9. Check the status of the **Nginx** service in the system.
10. Display Docker help and reference information.


### Solutions (Commands)

1. `docker search nginx`  
2. `docker images`  
3. `docker pull nginx`  
4. `docker run -d -p 8123:80 nginx`  
5. `docker ps`  
6. `docker stop <container_name>`  
7. `docker stop <container_ID>`  
8. `nginx -t`  
9. `systemctl status nginx`  
10. `docker --help`  


## Block 2. Docker `exec` Command (Working Inside a Container)

### Tasks

1. Start an interactive **bash** terminal inside a container.
2. Determine the current user inside the container.
3. Find the file **index.html** inside the container file system.
4. Display the contents of the specified file.
5. Delete a file inside the container.
6. Overwrite the contents of a file by entering text from the keyboard.
7. Get an interactive shell inside the container (alternative example).
8. Execute a single command inside the container without interactive mode.
9. View the list of processes inside the container.


### Solutions (Commands)

1. `docker exec -it <container_name> /bin/bash`  
2. `whoami`  
3. `find / -name index.html`  
4. `cat <filename>`  
5. `rm <filename>`  
6. `cat > <filename>`  
7. `docker exec -it my-container /bin/bash`  
8. `docker exec my-container ls -la`  
9. `docker exec my-container ps aux`  
