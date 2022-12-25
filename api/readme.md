### Command to build docker image

```shell
docker build -t myapp .
```

* where `myapp` is the name of the image
### Command to see all the images
```shell
docker images
```
### 1. Command to run an image
```shell
docker run myapp
```
### 2. Command to run an image
```shell
docker run --name myapp_c2 -p 4000:4000 myapp
```
where
* myapp_c2 is the name of the container
* left 4000 is the port we want to map to that on our computer
* right 4000 is port exposed by the container
### Command to see the list of running containers
```shell
docker ps
```
### Command to stop a container
```shell
docker stop myapp_c2
```
### Command to run the container without blocking terminal
```shell
docker run --name myapp_c2_ -p 5000:4000 -d myapp
```
* where -d means detached
### Command to restart a container
```shell
docker start myapp_c2
```