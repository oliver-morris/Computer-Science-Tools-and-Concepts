# Docker and Kubernetes

## Docker

Docker is used to make development and deployment easier. It allows you to package up code and run on a different machine with the knowledge of all the code and dependencies required to run the code. Docker consists of two main fundamentals: images and containers:

Images - the instructions on how to execute the code. It includes things like the technologies needed, runtimes and tools/instructions for running the code. They are composed of multiple immutable layers to form the complete image, each of which cannot be changed, only added upon with new layers.

Containers - where the code is ran. It is a lightweight, standlone unit that packages the code with the runtime and dependencies so that it can be run in different environments. This ensures if it works on your machine, it will work on all. All containers are isolated and containers work across different operating systems (OS) without any modifications. Unlike virtual machines (VMs) which virtualise the hardware and use the OS, containers virtualise the OS and shares the kernel which allows for quicker startups.

### Dockerfile
Contains the instructions to run the code and container. You should import the base image (typically operating systems or language runtimes e.g. node:24, ubuntu:latest).

You need to show where the working directory is.

Then you want to install the dependencies before importing the code. This is so layer caching is used correctly and you do not need to re-install the dependencies every time the code is updated.

You then should import the environment variables before establishing which port docker should use.

The final step should be the line to run the software.


### Dockerignore
This is so you don't copy every file over into the docker container

### Docker Scout
A nice docker tool which can be used in docker desktop or via the terminal to help find common vulnerabilities in the code.

### Examples CMD Lines:

Build the Image
`docker build -t docker_image_tag ./path-to-dockerfile`

Running the Container
`docker run -p computer_port:container_port docker_image_tag`

### Docker Compose and Volumes
When creating a project, you want to separate the different components into different containers e.g. one container for frontend, one for backend, one for database, etc. Docker compose is used to help multi-container applications communicate and run simultaneously. Docker volume is used for sharing data between containers and ensuring it is kept when a container is closed.

To do so, you need a `compose.yaml` file. This file contains a list of the services in the application. In here will link to the dockerfile of the main container and then some instructions such as the base image and any ports/environment variables for extra containers.

To start and stop all containers in a docker compose, you simply run:
`docker compose up`
`docker compose down`

### Docker Build Cloud
This is used for larger projects which may take longer to upload to docker every time. It can improve upload speeds by up to 39x and allows for sharing with others and sharing cache states.


## Resources
The Only Docker Tutorial You Need To Get Started - https://www.youtube.com/watch?v=DQdB7wFEygo
Docker Resources - https://www.docker.com/resources/

