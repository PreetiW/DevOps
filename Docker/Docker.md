# What and Why of Docker

Imagine a scenario where we finished developing the software and now we want to deploy it to production, In traditional ways we had to build the files ourselves and give the build and instructions about software and dependecies to operations team and it may happen there system might be different than ours and hence causing some issues while trying to do the same setup for deploying the code. Similar issue might also come when a new developer in the team is trying to setup the system. Hence to solve the issue docker was introduced.



# Docker and VMs

Docker is container based technology and containers are just user space of the operating system. At the low level, a container is just a set of processes that are isolated from the rest of the system, running from a distinct image that provides all files necessary to support the processes. It is built for running applications. In Docker, the containers running share the host OS kernel.

A Virtual Machine, on the other hand, is not based on container technology. They are made up of user space plus kernel space of an operating system. Under VMs, server hardware is virtualized. Each VM has Operating system (OS) & apps. It shares hardware resource from the host.


## Gotchas!

Linux OS natively supports containers and the technology Docker uses. For other OS you first need to install Docker Desktop Tool.

## Images & Containers - Basic Blocks of Docker

**Images** - The blueprint/template which contains code and required tools to run the code
**Containers** - The running unit of software (Running instances of images), we can create multiple containers based on one image

# Docker Commands

Note: Docker container lives as long as the process/application inside it is running, after that it exists

* docker run image_name  --> Runs a container from the image on the docker host, if the image is not present it will pull the image from dockerHub

* dpcker run image_name:tag --> Runs a container from the image with specified tag (version) from the docker hub or other registry, if we won't specify the default is latest

* docker run -it image_name --> Runs docker in the interactive mode and attached to terminal, as by default it won't be able to access the standard input of the terminal

* docker run -p 80:5000 image_name --> to access a webapp or app running inside the docker container on the host we can use docker container ip (each one gets an internal ip which is only accessible to docker host). To access it outside the docker host we will need to map the docker container ip to docker host by using port forwarding

* docker run -d image_name ---> To run the container in the detached mode in the background and we will be back in the terminal to continue other operations

* docker attach container id/name ---> To attach the container

* docker ps --> list all running containers and basic information about them, each container gets random id and name created by docker

* docker ps -a --> list all running and previously existed containers

* docker stop -->  to stop a contianer, provide container id or name

* docker rm --> to remove stopped containers permanantely to free up the space

* docker images --> to check all the images with their size details

* docker rmi image_name --> to remove an image from docker host, keep it mind to stop/delete all the containers which are using this image.

* docker pull image_name --> to only pull the image and not run the container

* docker exec container_name/id command_to_run --> to run a command on the docker container


