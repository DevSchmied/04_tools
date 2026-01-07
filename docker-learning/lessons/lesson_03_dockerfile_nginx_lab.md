## Task

Create a Dockerfile to build a container with the Nginx web server that meets the following requirements:

1. Use Debian as the base image.
2. Specify the image author information.
3. Update the operating system package list.
4. Install the Nginx web server without interactive prompts.
5. Declare a volume for storing web content.
6. Specify the port on which the application will accept incoming connections.
7. Configure Nginx to run in foreground mode when the container starts.


```dockerfile
FROM debian
MAINTAINER devschmied
RUN apt-get update
RUN apt-get install -y nginx
VOLUME /var/www/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]

