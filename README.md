# Docker
My learning on Docker and some projects using Docker

## **Why use Docker?**
Docker makes it really easy to run and install applications without worrying about dependencies or setup

## **What is Docker**
Docker is a platform or ecosystem around creating and running containers

### **Some Docker Terms**

**Image** - a single file with all dependencies and config required to run a program 

**Container** - Instance of an image to run the program. A set of process is isolated and  made available for the application

**DockerFile** - Configuration to define how our container should behave




### **Some basic Commands**

```docker run <image_name>``` -- *starts a container with the provided image*

Eg: docker run hello-world

```docker run <image_name> <default_command>```- *override the default command*

Eg: docker run busybox ls

```docker ps``` - *list running containers*

```docker ps --all``` - *list all the containers ever created*


```Docker create <image_name> < default>``` ---*create a container, not started*

Eg: docker create busybox ls

```Docker start -a <container ID>``` --- *start and print the output(-a)*

Eg: docker start -a asfsfsafasfsafaf


```docker system prune``` - *delete stopped container, build cache etc*

```docker logs <container ID>``` - *logs the output of the container.*

```docker stop <container ID>``` - *stop the container (SIGTERM) stop the process and shuts down container*

```docker kill <container ID>``` - *stop the conainer using SIGKILL, shut down abruptly*

```docker exec -it <container ID> <command>``` - *execute additional command in a container*

```-it```                                         *Allows us to provide input into the container*

Eg: docker exec -it assfasfsf bash

```docker run -it busybox sh``` - *directly start shell*

```docker build .``` - *to build docker image from dockerfile*

```Base Image``` - *Base OS with preinstall processes* 
