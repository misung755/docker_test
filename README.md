# dockerfiles-centos-user-adderable
ubuntu, It support base user creation and password setting.

# Building & Running

Copy the sources to your docker host and build the container, and to run.
```
	docker build --rm -t misung755/ubuntu .
	mkdir ~/df
	winpty docker run -it --name n1 -v c:\\Users\\user\\df:/var/www/html -p 80:80 misung755/ubuntu
```
Get the port that the container is listening on:

```
# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
ad2ad96e4b2f        nowage/centos7      "/bin/bash"         7 seconds ago       Up 6 seconds                            c1
```

To test, ("nowage" is username. )
```
	su - nowage
```
To Rollback
```
    docker rm c1 -f
    docker rmi nowage/centos7
```
Usage
