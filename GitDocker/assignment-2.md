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
3. docker images - Show a list of all images
```
% docker images
REPOSITORY               TAG       IMAGE ID       CREATED        SIZE
docker/getting-started   latest    157095baba98   6 months ago   27.4MB
hello-world              latest    46331d942d63   7 months ago   9.14kB
```
4. docker build - Build an image from a Dockerfile
```
% docker build -t myimage .
[+] Building 69.9s (10/10) FINISHED
..
```
5. docker run - Start a new Container from an Image and assign it a name and map a port
```
% docker run -d --name mycontainer1 -p 8080:80 myimage
7639d3ac4f40de1774929117c90081c2c6f79265f003527ace0b157bb90e7969
```
6. docker commit - Create an image out of container
```
% docker commit mycontainer1 dockerizebb/hello-world:testing
sha256:1aa6eb2a66ad7c45a7a6ebc9aa32a28f22dd2ff177ca2f6523f4fa12143f959a
```
7. docker login - Login to a registry
```
% docker login -u dockerizebb
Password: 
Login Succeeded
```
8. docker logout - Logout from a registry
```
% docker logout dockerizebb             
Removing login credentials for dockerizebb
```
9. docker push - Upload an image to a repository
```
docker push dockerizebb/hello-world:testing
The push refers to repository [docker.io/dockerizebb/hello-world]
1fbcfd681866: Pushed 
039f3e7df9ab: Pushed 
d5d1b4f5828c: Pushed 
49a73d776d4f: Pushed 
690134b62f80: Pushed 
9116b75921d2: Mounted from library/python 
7cec8790b395: Mounted from library/python 
528005faf52a: Mounted from library/python 
0e797936c0da: Mounted from library/python 
17dda7b58b9f: Mounted from library/python 
ce32a4d00d58: Mounted from library/python 
a589efb1139e: Mounted from library/python 
b162c19c7e1a: Mounted from library/python 
7346d8f0d212: Mounted from library/python 
testing: digest: sha256:4a7f6ac5470ac2375ac01282890417213229908ac5d527fdfd92892b5ca99567 size: 3259
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
10. docker ps - Show a list of running containers
```
% docker ps 
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS          PORTS                  NAMES
7639d3ac4f40   myimage   "uvicorn app.main:ap…"   38 minutes ago   Up 38 minutes   0.0.0.0:8080->80/tcp   mycontainer1
```
11. docker stop mycontainer1
```
% docker stop mycontainer1
mycontainer1
```
12. docker logs - Show the logs of a container
```
% docker logs mycontainer1
INFO:     Started server process [1]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
INFO:     Uvicorn running on http://0.0.0.0:80 (Press CTRL+C to quit)
INFO:     172.17.0.1:61644 - "GET /items/5?q=somequery HTTP/1.1" 200 OK
INFO:     172.17.0.1:61644 - "GET /favicon.ico HTTP/1.1" 404 Not Found
INFO:     172.17.0.1:61642 - "GET / HTTP/1.1" 200 OK
INFO:     Shutting down
INFO:     Waiting for application shutdown.
INFO:     Application shutdown complete.
INFO:     Finished server process [1]
```
13. docker diff - Show all modified files in container
```
% docker logs mycontainer1
INFO:     Started server process [1]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
INFO:     Uvicorn running on http://0.0.0.0:80 (Press CTRL+C to quit)
INFO:     172.17.0.1:61644 - "GET /items/5?q=somequery HTTP/1.1" 200 OK
INFO:     172.17.0.1:61644 - "GET /favicon.ico HTTP/1.1" 404 Not Found
INFO:     172.17.0.1:61642 - "GET / HTTP/1.1" 200 OK
INFO:     Shutting down
INFO:     Waiting for application shutdown.
INFO:     Application shutdown complete.
INFO:     Finished server process [1]
```
14. docker tag - Tag an image
15. docker rename - Rename a container
```
% docker rename mycontainer1 mycontainer2
```


## Assignment 3:
1. Create a hello world fastapi application.
2. Create a Dockerfile for your fastapi hello world application.
3. Build Docker image using Docker file.
4. Run docker image build in previous step.
5. Push your Docker image to Docker Hub.
```
https://hub.docker.com/repository/docker/dockerizebb/hello-world
```



## Assignment 4:
Automate Assignment below task using github action.
1. Build Docker Image 
2. Push Docker Image to Docker hub.
