<div align="center">

![Docker](https://github-repo-img.s3.eu-central-1.amazonaws.com/docker.png)

</div>

General Docker Commands

    docker version - Displays Docker version information.
    docker info - Shows system-wide information about Docker.
    docker help - Lists all Docker commands and options.

Working with Containers

    docker run -d --name my_container my_image - Runs a container in detached mode with a specified name.
    docker ps - Lists all running containers.
    docker ps -a - Lists all containers (including stopped ones).
    docker stop my_container - Stops a running container.
    docker start my_container - Starts a stopped container.
    docker restart my_container - Restarts a running or stopped container.
    docker rm my_container - Removes a stopped container.
    docker exec -it my_container /bin/bash - Accesses a running container with an interactive terminal.

Image Management

    docker images - Lists all Docker images on your system.
    docker pull ubuntu - Downloads an image from Docker Hub (e.g., Ubuntu).
    docker build -t my_image . - Builds a Docker image from a Dockerfile in the current directory.
    docker rmi my_image - Removes an image.
    docker tag my_image my_repo/my_image:latest - Tags an image with a repository name and version.
    docker push my_repo/my_image:latest - Pushes an image to a Docker registry.

Volume Management

    docker volume create my_volume - Creates a named volume.
    docker volume ls - Lists all Docker volumes.
    docker volume inspect my_volume - Displays details about a specific volume.
    docker volume rm my_volume - Removes a volume.

Network Management

    docker network ls - Lists all Docker networks.
    docker network create my_network - Creates a new network.
    docker network inspect my_network - Shows details about a network.
    docker network connect my_network my_container - Connects a container to a network.
    docker network disconnect my_network my_container - Disconnects a container from a network.

Docker Compose Commands

    docker-compose up - Starts services defined in a docker-compose.yml file.
    docker-compose down - Stops and removes containers, networks, and volumes defined in a docker-compose.yml.
    docker-compose build - Builds the services specified in the docker-compose.yml.
    docker-compose logs - Displays logs from all services.
    docker-compose ps - Lists containers created by Docker Compose.

Container Logs and Monitoring

    docker logs my_container - Shows logs of a specific container.
    docker top my_container - Displays processes running inside a container.
    docker stats - Shows real-time stats of all running containers.
    docker inspect my_container - Displays detailed information about a container in JSON format.

Docker Cleanup Commands

    docker system prune - Cleans up unused containers, networks, images, and build cache.
    docker container prune - Removes all stopped containers.
    docker image prune - Deletes unused images.
    docker volume prune - Removes all unused volumes.
    docker network prune - Deletes all unused networks.

Docker Registry Commands

    docker login - Logs in to a Docker registry.
    docker logout - Logs out of a Docker registry.
    docker push my_repo/my_image - Pushes an image to the Docker registry.
    docker pull my_repo/my_image - Pulls an image from the Docker registry.

Docker Export and Import

    docker save -o my_image.tar my_image - Saves an image to a tar archive.
    docker load -i my_image.tar - Loads an image from a tar archive.
    docker export -o my_container.tar my_container - Exports a container’s filesystem as a tar archive.
    docker import my_container.tar - Creates an image from a tar archive.

Debugging and Troubleshooting

    docker logs my_container - Retrieves logs from a running container.
    docker events - Streams Docker events in real time.
    docker inspect my_container - Provides detailed information about a container or image.
    docker diff my_container - Shows changes in a container’s filesystem.
    docker exec -it my_container /bin/sh - Opens an interactive shell inside a running container for debugging.
