Hypervisor is software that helps to create virtual machines.
Using Hypervisor we can create multiple virtual machines (vms) on top of a physical machine
---------------------------------------------------------------------------------------------
* what is Docker
--> "Docker is an open source containerization platform."

--> Docker is a platform designed to make it easier to create, deploy, and run applications
     by using containers.
--> Container Engines like Docker can be installed on the operating system and create containers.
--> Container is an isolated area which contains everything necessary to run your application.

* Genaral Definition

--> a person employed in a port to load and unload ships.
-----------------------------------------------------------------------------------------------
* what is container 

--> container is a isolated area which will have the application required and it have its 
    own hard disk ,network interface ,users, process tree.
--> Every containeris an isolated area.
--> we can also place restrictions to use only less amount of ram and storage
--> that isolated area is known as container. 
--> Containers are very lightweight in nature.
-----------------------------------------------------------------------------------------------
* whenever the docker installed  on virtual machine a "docker" group was created.
------------------
* what is containerazation
------------------
* the process of runnning application in the container is known as containerazation
----------------------------------------------------------------------------------------------
* Why Docker containerss are called lightweight in nature?


*  Docker containers are designed to be minimal, only including what is necessary for 
   the application to run ,further reducing their size.
* Docker solves complexity.
* Dockerd receives the requests from the client. Dockerd is also known as heart for Docer.
* Dockerd is known as Docker Demon.
* Docker hub is a public registry.
* Registry is a place where all the docker images are stored.
* Registry is a platform which can be shared by Docker images Whether it is a public registry 
   or private registry.
* "Dockerfile" is a file where you provide the steps to build your Docker Image which is Set up instructions.
* applications requiring software like java need not be present on the docker host
      (linux machine where docker is installed), they are present in container
* CGroups - by using cgroups we can put restrictions for container to use particular space,ram,cpus
--------------------
 Dockerfile

* FROM: Choosing the base image
* RUN: Executing a command during image build
* CMD and ENTRYPOINT: BOTH are start comands to start the application.(The full form of
                       CMD in Docker is Command. It is an instruction in a Dockerfile
                       that specifies what command to run when a  container is started.)
* Expose: This instruction exposes ports for tcp or udp


*  Docker containers are created from Docker images. An image is a read-only template 
    that contains everything needed to run an application, including the code, runtime, 
    libraries, and dependencies. Images are built using Dockerfiles, which are text 
    files containing instructions for building the image.

* Difference Between CMD and entry point.
  
    CMD is a default command that can be overridden when the container is started.
    This means that you can specify a different command to run when you start the 
    container using the docker run command.
    ENTRYPOINT is a command that cannot be overridden when the container is started.
    This means that the specified command will always run when the container is 
    started, regardless of what you specify in the docker run command.
    
* 