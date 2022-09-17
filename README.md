# docker-bgd

##Commands

###Docker Version
```
docker --version
```

###Show all containers

```
docker ps -a
```

###Show running containers

```
docker ps
```

###Show all images

```
docker images
```

###Download image from dockerhub

```
docker pull image-name
```

###Run a container based on image

```
docker run image (hellow-world)
```

###Run a container based on image with tag

```
docker run image:tag
docker run hellow-world:latest
```

###Delete container by id
```
docker rm container-id
```

###Connect to process into container

```
docker run -it image (busybox)

it - interactive terminal
```

###Connect to process into a container in background

```
docker run -d image (busybox)

d - detached
```

###Stop container

```
docker stop container-id
```

###Stop hardest

```
docker kill container-id 
```

###Remove all containers

```
docker container prune [y]
```

###Inspect docker container

```
docker container inspect container-id

docker container inspect container-id | grep IPAddress
```

###Interactive process inside container

```
docker exec -it container-id bash
```

###Naming containers

```
docker run -d --name container-name image
```

###Remove container on stop

```
docker run --rm image
```

###Separation of commands on rows

```
docker run \
-v ${PWD}:/usr/share/nginx/html \
-p 8081:80 \
-d \
--rm \
nginx
```

##Port mapping

```
docker run -p 8080:80 image

p - publish
8080 - external port
80 - internal port
```

##Volume mapping

```
docker run -v folder-path-outside:folder-path-inside image

docker run -v ${PWD}:/usr/share/nginx/html -p 8080:80 -d nginx
```