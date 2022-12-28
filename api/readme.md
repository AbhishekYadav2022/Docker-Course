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
### Command to see all the containers
```shell
docker ps -a
```
### Command to remove an image
```shell
docker image rm myapp
```
### Command to remove an image **forcibly**
```shell
docker image rm myapp -f
```
### Command to see all the images
```shell
docker images
```
### Command to remove a container
```shell
docker container rm myapp_c2
```
### Command to remove many containers at the same time
```shell
docker container rm con1 con2
```
### Command to remove all containers, all images and all volumes
```shell
docker system prune -a
```
### Command to create an image with tag
```shell
docker build -t myapp:v1 .
```
### Command to create a container with tag
```shell
docker run --name myapp_c -p 4000:4000 myapp:v1
```
### Command start a container in attached mode
```shell
docker start -i container_name
```
### Command start a container in attached mode
```shell
docker start -i container_name
```
### Command to atomatically delete a container after stopping it
```shell
docker run --name myapp_c_nodemon -p 4000:4000 -rm myapp:nodemon
```
### Command to use volume
```shell
docker run --name myapp_c_nodemon -p 4000:4000 --rm -v C:\Users\abhishek\Desktop\My-Codes\Docker\api:/app -v /app/node_modules myapp:nodemon
```
### Command to run docker-compose
```shell
docker-compose up
```
### Command to stop docker-compose
```shell
docker-compose down
```