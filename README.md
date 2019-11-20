# Docker-Kubernetes-Guide
Complete Docker and Kubernetes Guide.

## **Docker Installation**
***

Firstly open the terminal and follow these command step by step.
> **sudo apt-get update**

>**sudo apt-get install docker.io**

After installation check the version and info **(For complete information)**.
>**docker --version**

> **sudo docker info**

For checking the components of docker use the following command **(Two components will show after run this command if one show so there is na error in installation)**.

>**sudo docker version**

## **Pulling Images in Docker**
***
>**sudo docker image pull alpine:latest**

>**sudo docker image aamirpinger/helloworld:latest**

- You can also use following command instead of the previous.
> **sudo docker pull alpine:latest**

- Now to see what images you have in your system.
> **sudo docker image ls**
- You can also use **sudo docker images** isteal of the previous. 
- Image ID of any image will be unique.
  
## **Removing any Image in Docker**
***
- For all image just like we do for alpine:latest 
> **sudo docker image rm alpine:latest**

## **Running Container**
***
- To run a container from an image in an interactive mode(it). Two mode sh for shell and the other one is bash mode.
>**sudo docker run -it aamirpinger/helloworld sh**
- After run this command you are in file system of your given containerized Application.
- Use **ls** command to see the list of files in the current file system.
- Use **exit** command to exit the file system **(Changing running state to stop state)**.
## **Listing of container in any State**
***
- Use these command to show all the containers while in running and stop state.
- Use **Ctrl+p+q** to stop the container not exit it .
>**sudo docker container ls -a**

>**sudo docker ps -a**

## **Want to in the running container**
***

>**sudo docker exec -it anyname**

- Where any name defined as a Conatiner name which is randomly generated when you start a container **(Unique name for all container)** write the name of the conatiner which you want to go again in that file system.

## **Stopping and Starting Container**
***
- Where container id  and name is unique for all the containers use one of them.
> **sudo docker container stop ContainerID/Name**

- Similary specify container id or name to start a stop container.
> **sudo docker start ContainerID/Name**