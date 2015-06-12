```

 $ docker run -t -i ubuntu:14.04 /bin/bash
     Run a command in a new container
     uses ubuntu:14.04 image (will download if not found locally)
     -t assign a pseudo-tty
     -i interactive mode (grabs STDIN)
     
 $ docker run -d -p 80:80 training/webapp python app.py
     Run a webserver
     -p bind network ports (host:container)
  
 $ docker ps [-a]
     List containers
     -a show all containers, also the ones currenty not running
     
 $ docker logs -f nostalgic_morse
     Fetch the logs of a container (STDOUT)
     -f follow log output (similar to tail -f)

 $ docker start -a nostalgic_morse
     Start one or more stopped containers
     -a Attach container's STDOUT/STDERR and forward all signals to the process
     
 $ docker stop nostalgic_morse
     Stop a container by sending SIGTERM and then SIGKILL after a grace period
     
 $ docker images [-a]
     List images on the host
     -a show all images
  
 $ docker build -t myimage .
     Build a new image from the Dockerfile in the current directory
     -t repository name and tag
 
 $ docker tag 5db5f8471261 myimage2
     Tag an image into a repository
     
     
Example Docker File:
# DOCKER-VERSION 1.6.2
FROM ubuntu:14.04
MAINTAINER blip

# Install Apache and PHP
ENV http_proxy http://example.com:3128
RUN apt-get -y update
RUN apt-get install -y apache2 php5 libapache2-mod-php5

# Add data file
ADD html /var/www/html
RUN rm /var/www/html/index.html
VOLUME /var/www/html

# Add launch scripts
ADD run_all /root/scripts/run_all
ADD apache /root/services/apache

# Start Apache
EXPOSE 80
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
#ENTRYPOINT /root/scripts/run_all
```
