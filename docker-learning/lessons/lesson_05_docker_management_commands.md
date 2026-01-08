## Tasks
1. Display a list of running containers.
2. Display the list of the entire container history, including stopped containers.
3. Remove a container by its identifier (7b6eef994cd5).
4. Stop a container by its identifier (b2d5a0d52d59).
5. Forcefully remove a container by its identifier (f3ef5dee0e74), even if it is currently running (a flag is used).
6. Display a list of identifiers of all containers (flags are used).
7. Clean up the entire container history, including stopped containers (command substitution is used).
8. Display a list of available Docker images.
9. Remove a Docker image by its name (hello-world).
10. Remove a Docker image by its identifier (3e4394f6b72f).
11. Remove all stopped containers (a cleanup command is used).
12. Remove all unused Docker images.
13. Remove all unused Docker images, including those not associated with any container (a flag is used).


## Commands to complete the tasks

1. `docker ps`
2. `docker ps -a`
3. `docker rm 7b6eef994cd5` 
4. `docker stop b2d5a0d52d59`
5. `docker rm f3ef5dee0e74 -f`
6. `docker ps -aq`
7. `docker rm $(docker ps -aq)`
8. `docker images`
9. `docker rmi hello-world`
10. `docker rmi 3e4394f6b72f`
11. `docker container prune`
12. `docker image prune`
13. `docker image prune -a`