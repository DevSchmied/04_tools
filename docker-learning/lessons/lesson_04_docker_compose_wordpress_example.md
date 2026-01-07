## Task

Create a docker-compose.yml file to deploy a WordPress web application with a MariaDB database that meets the following requirements:

1. Use Docker Compose file format version 3.8.
2. Define a MariaDB service using the official Docker image with a specified version:
   - set the database name for WordPress;
   - create a dedicated database user;
   - set a password for the database user;
   - set a root user password.
3. Attach a volume for persistent storage of MariaDB database data.
4. Define a WordPress service using the official Docker image with Apache and PHP.
5. Configure WordPress to connect to the MariaDB database using:
   - the database service name as the host;
   - the database name;
   - the database user;
   - the database user password.
6. Ensure the correct startup order by defining a dependency of the WordPress service on the MariaDB service.
7. Publish the WordPress web application on the host machine by mapping container port 80 to host port 8080.
8. Attach a volume for storing WordPress site files (themes, plugins, uploads) to ensure data persistence across container restarts.


## Solution

```yml
version "3.8"

services:
  mariadb:
    image: mariadb:11

    environment:
      MYSQL_DATABASE: wordpress 
      MYSQL_USER: wp
      MYSQL_PASSWORD: wp_pass
      MYSQL_ROOT_PASSWORD: root_pass
  
    volumes:
      - ./database:/var/lib/mysql

  wordpress:
    image: wordpress:php8.2-apache
    depends_on:
      - mariadb
    ports:
      - "8080:80"
    environment:
      WORDPRESS_DB_HOST: mariadb:3306
      WORDPRESS_DB_NAME: wordpress
      WORDPRESS_DB_USER: wp
      WORDPRESS_DB_PASSWORD: wp_pass
    volumes:
      - ./html:/var/www/html
