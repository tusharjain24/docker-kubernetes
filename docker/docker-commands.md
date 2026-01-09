# Docker Commands

## Docker Images

- `docker images` -> List all images
- `docker pull <image_name>` -> Pull image from repository(docker hub)
- `docker rmi $(docker images -q)` -> Remove all images
- `docker rmi <image_id>` -> Remove specific image
- `docker rmi <image_name>` -> Remove specific image

## Docker Containers

- `docker ps` -> List all containers
- `docker ps -a` -> List all containers (including stopped)

### Container Management
- `docker rm <container_id>` -> Remove specific container
- `docker rm <container_name>` -> Remove specific container
- `docker rm $(docker ps -a -q)` -> Remove all containers
- `docker rm -f <container_id>` -> Remove specific container (force)
- `docker rm -f $(docker ps -a -q)` -> Remove all containers (force)

### Container Run
- `docker run -d <image_name>` -> Run container in detached mode
- `docker run -it <image_name>` -> Run container in interactive mode
- `docker run -it --name <container_name> <image_name>` -> Run container with specific name
- `docker run -it -d --name <container_name> -p <host_port>:<container_port> <image_name>` -> Run container in detached mode with specific name and port
- `docker exec -it <container_name> /bin/bash` -> Run command in container

### Container Start/Stop
- `docker start <container_id>` -> Start specific container
- `docker start <container_name>` -> Start specific container
- `docker stop <container_id>` -> Stop specific container
- `docker stop <container_name>` -> Stop specific container
- `docker restart <container_id>` -> Restart specific container
- `docker restart <container_name>` -> Restart specific container
- `docker stop $(docker ps -q)` -> Stop all containers
