# Docker & Docker Hub


## Assignment 1:
Demonstrate minimum 15 basic docker command with explanation and screenshot.

1. docker pull - Download an image
```
% docker pull hello-world 
Using default tag: latest
latest: Pulling from library/hello-world
7050e35b49f5: Pull complete 
Digest: sha256:18a657d0cc1c7d0678a3fbea8b7eb4918bba25968d3e1b0adebfa71caddbc346
Status: Downloaded newer image for hello-world:latest
docker.io/library/hello-world:latest
```
2. docker run - Start a new Container from an Image
```
% docker run hello-world

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (arm64v8)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
 ```
3. docker images - Show a list of all containers
```
% docker images
REPOSITORY               TAG       IMAGE ID       CREATED        SIZE
docker/getting-started   latest    157095baba98   6 months ago   27.4MB
hello-world              latest    46331d942d63   7 months ago   9.14kB
```


## Assignment 2:
Run Hello World Docker Image Locally.
```
% docker pull hello-world 
Using default tag: latest
latest: Pulling from library/hello-world
7050e35b49f5: Pull complete 
Digest: sha256:18a657d0cc1c7d0678a3fbea8b7eb4918bba25968d3e1b0adebfa71caddbc346
Status: Downloaded newer image for hello-world:latest
docker.io/library/hello-world:latest

% docker run hello-world

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (arm64v8)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
 ```

## Assignment 3:
Create a hello world fastapi application.
Create a Dockerfile for your fastapi hello world application.
Build Docker image using Docker file.
Run docker image build in previous step.
Push your Docker image to Docker Hub.


## Assignment 4:
Automate Assignment below task using github action.
1. Build Docker Image 
2. Push Docker Image to Docker hub.