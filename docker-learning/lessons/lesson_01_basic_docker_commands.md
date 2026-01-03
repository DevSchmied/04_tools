## Tasks

1. Find a way to display help and documentation for available Docker commands.
2. Determine how to view a list of containers that are currently running.
3. Learn how to display a list of all containers, including stopped ones.
4. Find out how to list images available locally on the system.
5. Run the first test container and analyze the result of its execution.
6. Explore how to search for images in the public Docker registry.
7. Understand how to download an image from a remote registry to the local machine.
8. Learn how to stop a running container.
9. Find out how to remove a container after it has been used.
10. Understand the difference between removing a container and removing an image.
11. Learn how custom images are created using instructions from a configuration file.
12. Find out how to execute a command inside an already running container.

---

## Solution

1. `docker --help`
2. `docker ps`
3. `docker ps -a`
4. `docker images`
5. `docker run hello-world`
6. `docker search image-name`
7. `docker pull image-name`
8. `docker stop container-name`
9. `docker rm container-name`
10. `docker rmi image-name`
11. `docker build`
12. `docker exec`