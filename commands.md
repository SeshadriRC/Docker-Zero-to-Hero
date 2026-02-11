# Docker Commands

Some of the most commonly used docker commands are 

### docker commit

- Creat a image from the existing container

```bash
docker commit <container-name> <my-imagename:tag>
docker commit mycontainer myimage:v1
```

### docker images

Lists docker images on the host machine.

### docker build

Builds image from Dockerfile.

### docker run

Runs a Docker container. 

There are many arguments which you can pass to this command for example,

`docker run -d` -> Run container in background and print container ID
`docker run -p` -> Port mapping

use `docker run --help` to look into more arguments.

### docker ps

Lists running containers on the host machine.

### docker stop

Stops running container.

```
docker stop <container-id>
```

### docker start

Starts a stopped container.

```
docker start <container-id>
```

### docker rm

Removes a stopped container.

### docker rmi

Removes an image from the host machine.

### docker pull

Downloads an image from the configured registry.

### docker push

Uploads an image to the configured registry.

```bash
# Below is the syntax
docker tag <local-image> <dockerhub-username>/<repo-name>:<tag>

# Outputs
PS E:\ubuntu-data\docker> docker images
                                                                                                                            i Info →   U  In Use
IMAGE                           ID             DISK USAGE   CONTENT SIZE   EXTRA
ubuntu:latest                   cd1dba651b30        119MB         31.7MB    U 

# sesharc is my docker username having the latest tag
PS E:\ubuntu-data\docker> docker tag ubuntu:latest sesharc/ubuntu:latest
PS E:\ubuntu-data\docker> docker push sesharc/ubuntu:latest

i Info → Not all multiplatform-content is present and only the available single-platform image was pushed

```

### docker exec

Run a command in a running container.

### docker network

Manage Docker networks such as creating and removing networks, and connecting containers to networks.
