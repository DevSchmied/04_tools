## Task

1. Which Docker instruction defines the base image.
2. The instruction that executes commands during the image build process.
3. Instructions that copy files and directories into a Docker image.
4. The instruction used to set the working directory inside the container.
5. The instruction that specifies which ports the container uses.
6. Instructions that define the command used to start the container.

## Solution

1. `FROM`
2. `RUN`
3. `COPY` / `ADD`
4. `WORKDIR`
5. `EXPOSE`
6. `CMD` / `ENTRYPOINT`


## Task

1. Display the contents of the Dockerfile in the terminal.
2. List all local Docker images.
3. Build a Docker image based on the instructions in the Dockerfile and:
   - specify the image name using a flag.
4. Display the contents of the current directory after building the image.
5. Run a container from the created image and:
   - start the container in detached mode using a flag;
   - map a host port to a container port using a flag.
6. Display a list of running containers.


## Commands

1. `cat Dockerfile`
2. `docker images`
3. `docker build -t myapp .`
4. `ls`
5. `docker run -d -p 8080:80 myapp`
6. `docker ps`

