# General Commands
Check Docker version
```
docker -v
```
Display information about Docker
```
docker info
```
Download an image from Docker Hub
```
docker pull <image_name>
```
List the local Docker Images
```
docker images
```
List running containers
```
docker ps
```
List all containers (also stopped containers)
```
docker ps -a
```
Create and run a new Docker container
```
docker run <Options> <Image>
```

# Container Life Cycle
Start a stopped container
```
docker start <container_name>
```
Stop a running container
```
docker stop <container_name>
```
Force a container to stop
```
docker kill <container_name>
```
Restart a container
```
docker restart <container_name>
```
Remove a stopped container
```
docker rm <container_name>
```

# Images
Build a Docker image from a Dockerfile
```
docker build -t <image_name> <path_to_dockerfile>
```
Remove an image
```
docker rmi <image_name>
```
Remove all unused images
```
docker image prune
```

# Docker Compose
Start a containers out of a Docker Compose file
```
docker-compose up
```
Stop and remove container out of a Docker Compose file
```
docker-compose down
```
List all container and there status
```
docker-compose ps
```

# Volumes
Create a named volume
```
docker volume create <volume_name>
```
Mount a volume to a container
```
dokcer run -v <volume_name>:<container_path>
```
List all volumes
```
docker volume ls
```
Remove a volume
```
docker volume rm <volume_name>
```

# Network
Create a user.defined network
```
docker network create <network_name>
```
List all networks
```
docker network ls
```
Connect a container to a network
```
docker network connect <network_name> <container_name>
```
Disconnect a container from a network
```
docker network disconnect <network_name> <container_name>
```

# Docker Registry and Hub
Log in to a Docker registry
```
docker login
```
Push an image to a registry
```
docker push <image_name>
```
Pull an image from a registry
```
docker pull <image_name>
```

# Logs and Debuging
Show the log of a docker container
```
docker-compose logs <container_name>
```
Run a command in a running container
```
docker-compose exec <container_name> <comamnd>
```
Start an shell in a running container
```
docker exec -it <container_name> /bin/bash
```
Show usage of running container
```
docker stats <container_name>
```

# Cleanup
Remove all stopped containers, unused networks and images
```
docker system prune
```
Remove all stopped containers
```
docker container prune
```
Remove all unsused images
```
docker image prune
```
Remove all unused Volumes
```
docker volume prune
```
```
