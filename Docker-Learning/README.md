## Handling Containers (The "Running" Parts)
- ```docker run <image>``` Create and start a container from an image.
- ```docker run -d <image>``` Detached mode: Runs the container in the background.
- ```docker run -p 8080:80 <image>``` Port Mapping: Maps Host Port 8080 to Container Port 80.
- ```docker ps``` List all running containers.
- ```docker ps -a``` - List all containers (including stopped ones).
- ```docker stop <name/id>``` Gracefully stop a running container.
- ```docker rm <name/id>``` Delete a container (must be stopped first).
- ```docker rm -f <name/id>``` Force delete a container even if it's running.

## Managing Images (The "Templates")

- ```docker images``` List all images currently downloaded on your machine.
- ```docker pull <image>``` Download an image from Docker Hub without running it.
- ```docker rmi <image>``` Delete an image from your local machine.
- ```docker build -t <name> .``` Build your own image from a Dockerfile in the current folder.

## Inspecting & Debugging

- ```docker logs <name/id>``` See the console output (logs) of a container.
- ```docker logs -f <name/id>``` Follow logs in real-time (like a live stream).
- ```docker exec -it <name/id> sh``` Open a terminal inside the running container.
- ```docker inspect <name/id>``` See all the technical "under the hood" details of a container.

## Housekeeping

- ```docker system prune``` The Nuke: Deletes all stopped containers and unused images to save space.