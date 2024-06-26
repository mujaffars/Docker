# Docker

1. List Docker Images
To verify that your image has been created successfully, you can list all Docker images:
#### sudo docker images

2. Run a Container from the Image
To run a container based on your my-app image, use the docker run command:
#### sudo docker run -d --name my-app-container -p 8080:8080 my-app

In this command:
-d runs the container in detached mode (in the background).
--name my-app-container names the container my-app-container.
-p 8080:8080 maps port 8080 on the host to port 8080 in the container (adjust as needed).

3. Check Running Containers
To see if your container is running, use:
#### sudo docker ps
This will list all currently running containers.

4. Access the Running Container
If you need to get a shell inside the running container, you can use docker exec:
#### sudo docker exec -it my-app-container /bin/bash

5. View Container Logs
To view the logs of your running container, use:
#### sudo docker logs my-app-container

6. Stop and Remove the Container
To stop the running container, use:
#### sudo docker stop my-app-container

To remove the stopped container, use:
#### sudo docker rm my-app-container

7. Remove the Docker Image
If you need to remove the Docker image, use:
#### sudo docker rmi my-app

8. Clean Up Unused Images, Containers, Volumes, and Networks
To clean up unused Docker objects, you can use:
#### sudo docker system prune -a
