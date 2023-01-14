# All About Docker

## What is Docker

Docker is a tool that allows us to test and deploy applications easily. Docker is helping to run our application in an isolated environment. A developer assigns applications in a docker file which is used to build Docker images that also assigns a Docker container. This also ensures that your application will run in any environment.

## Why use Docker?

Using Docker can help you to deliver your code faster, and gives you control over many applications. Docker helped us in using applications more popular. It allows us to use applications in a single operating system. You can use Docker for Data Processing, Delivery, and Containers as a Service. Let us take an example if you are giving a hackathon and you don't want to download Mysql on your pc then you can simply run the docker command it will make your work easier.

## What is Virtualization?

This is a process in which multiple virtual environments can be created all of them have their own operating system. All of these virtual environments are created on top of the host operating system. Multiple virtual machines are created with the help of Hypervisor and also manage them.

## What is Containerization?

This is a process in which an application is enveloped with all the dependencies and configurations required to run the application in any environment. In containerization, the containers are created on top of the host operating system.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673715800984/c13fb306-79c6-4f20-83e0-2cca2d275b75.png align="center")

## Docker Architecture

### **Docker runtime**:-

Runtime allows us to start and stops the container

It is of Two types -

* **low-level runtime** - it works with the operating system and starts and stops the container.
    
* **container d**\- Managing run c helps us to pull the images from the source. It's also used in the Kubernetes runtime.
    
    ### **Docker engine:-**
    
    Docker Engine acts as a client-server application with A server with a long-running daemon process docked. APIs specify interfaces that programs can use to talk to and instruct the Docker daemon.
    
    ### **Docker Daemon**:-
    
    It is the service that runs on your operating system. the docker daemon includes all the data in a single directory. This helps us to track everything related to docker which includes docker images, and docker containers
    
    ### **Docker CLI:-**
    
    This is the primary way that users interact with Docker. When you use the commands such as docker run hello-world, then the clients send these commands to docker which carries them out and gives us the whole output. The docker command uses the docker API. The docker client can also communicate with more than one Docker daemon.
    
    ### **Docker Registries:-**
    
    Docker registry stores docker images. There is a public registry called Docker Hub that anyone can use, and Docker is basically specific to looking for images on Docker Hub. You can even run your private registry.
    
    ### **Docker objects**:-
    
    When you use Docker, you are creating and using images, containers, networks, volumes, plugins, and other objects.
    
    ### **Images**:-
    
    Images are just the read-only template that gives instructions to create a Docker container.
    
    ### **Containers -**
    
    A container is a runnable instance of an image. You can create, start, stop, move, or delete a container using the Docker API or CLI. You can connect a container to one or more networks, attach storage to it, or even create a new image based on its current state. A container is relatively well isolated from other containers and its host machine. You can control how isolated a container’s network, storage, or other underlying subsystems are from other containers or from the host machine.
    

## Docker Commands

docker In the docker CLI it's going to the server and says run hello-world run - It is you run an image to create a container. hello-world - This is the name of the image. When you run this command on your terminal it will give you the output, It will say unable to find image 'hello-world' Then docker will reach the docker registry, It will run that image in your terminal and then show you the final output.

```bash
docker run hello-world
```

Docker runs in the interactive environment of ubuntu. If ubuntu is already installed or present on your pc, then it will not give you any error.

```bash
docker run -it ubuntu
```

This command will show you all the docker images present on your pc. It will show you those images which are already downloaded to your pc.

```bash
docker images
```

## How does a docker image work?

A Docker image contains operating system files and also dependencies for any application, A Docker Image specifies a sequence of steps required to perform a particular task. That task could be to run a web server or send an email or whatever you can make a computer do. An Image can be built manually by running the commands step-by-step against the Docker daemon.

## Additional Docker commands

This command will let you know about the containers that are currently running.

```bash
docker ps
```

This command will tell the list of the containers which are present in your pc.

```bash
docker container ls
```

You can use this command to stop the particular container which you wanna stop. Just type the command followed by their id.

```bash
docker stop
```

You can run this command to see all the stopped containers.

```bash
docker ps -a
```

You can use this command to remove the container just by writing the command followed by its id.

```bash
docker rm
```

This command will help you know everything about the container. Its id, path, where it is currently running, process id, everything

```bash
docker inspect ubuntu
```

This command will show all those containers which are stopped. Prune is basically the command which are deleting all the stopped containers.

```bash
docker container prune -f
```

This command will download and ping the particular website.

```bash
docker run alpine ping www.wikipidea.com
```

This command will help you to run the particular website in the background

```bash
docker run -d alpine ping www.wikipidea.com
```

This command will run the ubuntu and also its gonna show the Hello in your terminal.

```bash
docker run ubuntu echo Hello
```

This command will remove the alpine image from the container.

```bash
docker rmi alpine -f
```

## Resources

[Kunal Kushwaha Youtube](https://www.youtube.com/watch?v=17Bl31rlnRM&t=3434)

## Thankyou so much for reading