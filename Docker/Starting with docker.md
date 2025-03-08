
# Installing 
are you retarded? 
# initializing a docker container
you can install an official docker image of something you want to use, but in the case of creating it, you will have to create a "DockerFile" in the project and write code in it to configure it to build an image so that it could be used later anywhere and could be uploaded to docker hub.

# the difference between an image and a container
an image is a blueprint for the container. you can run multiple identical containers using the same image.
the purpose of docker is to run applications, so the docker image i have for SQL servers is as if SQL servers are running on my device.

# Deleting a container
to delete a container use:

```
docker rm <container name>
```

# Stopping a docker container
```
docker stop <cont-name>
```
# some commands
the only way to learn is to try

to see all images use: `docker images`.

to create a container using an image use: `docker run <image name>`.
to see all running containers use: `docker ps`.




# Resources

[Docker Documentation ](https://docs.docker.com/get-started/introduction/)



