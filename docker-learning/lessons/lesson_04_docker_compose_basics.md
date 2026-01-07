## Task

1. Install the docker-compose package on the system.
2. Review the brief help information for docker-compose commands.
3. Create a new directory for the project.
4. Navigate to the created project directory.
5. Create a docker-compose.yml file to define services.
6. Verify the presence of the created files and directories.
7. Start the project defined in the docker-compose.yml file in detached mode.
8. Display the contents of the docker-compose.yml file in the terminal.

## Solution

1. `sudo apt install docker-compose -y`
2. `docker compose --help`
3. `mkdir wp_site`
4. `cd wp_site/`
5. `nano docker compose.yml`
6. `ls`
7. `docker compose up -d`
8. `cat docker compose.yml`


## Task

1. Start all services (containers) defined in the docker-compose.yml file.
2. Stop and remove all running services along with their associated containers.
3. View the current status of Docker Compose services.
4. View the logs of all Docker Compose services.

## Solution

1. `docker compose up`
2. `docker compose down`
3. `docker compose ps`
4. `docker compose logs`