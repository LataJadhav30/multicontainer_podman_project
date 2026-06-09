#MultiContainer Web Application using podman on RHEL9

###Overview 
This project demonstrates a multicontainer deployment using podman on RHEL9.

##Technologies Used
-RHEL9
-Podman
-MariaDB
-Apache/Python HTTP Server
-Containerfile
-Podman pods

## Project Architecture
  
  Browser
    |
 Web Container
    |
 Podman Pod
    |
MariaDB Container

## Features
-Containerized Web Application
-MariaDB Database
-Podman Pod
-Persistent Storage
-Firewall Configuration

####Commands Used

##Build image

podman build -t myweb:v1

## Create Pod

podman pod create --name webpod -p 8080:8080

## Run web container

podman run -d --pod webpod --name mariadb \
-e MYSQL_ROOT_PASSWORD=REDHAT123 \
-e MYSQL_DATABASE=projectdb \
docker.io/library/mariadb:latest


###Author

Lata N Jadhav

Red hat certified System Administration (RHCSA) Cerified
Red hat certified specilist in Containers(DO188)


