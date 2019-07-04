# Pull Command
>Used to pull image from ***~Docker hub ~***
~~~
docker pull **ubuntu:latest**
docker pull imagename:tag
~~~

# Images Command
>Used see pulled images
~~~ 
docker images
~~~
# Remove unsed images 
>Removes images from disk, **cannot remove images which have running or *stopped* containers.**
~~~
docker rmi ***image name***
docker rmi ***image id***
~~~
## Remove unused containers
~~~
docker rm ***container name***
docker rm ***container id***
~~~
***

# Run Command
>Used to run image from command
~~~
docker run ubuntu:latest
~~~
Image if not in the disk, will be pulled from dockerhub for first use.

## Various options for run command

-i : Maps the host system's bash(input/output) to that of the container.

-it : Starts container with terminal

>Port Mapping: To map container port to host port use: -p 
### **-p** ***host-port-number***:***container-port-number***
~~~
docker run ubuntu -p 80:8000
~~~
>Volume mapping: To map dirctory path in host machine to a directory in container use: -v
### **-v** ***host-directory-path***:***container-directory-path***
~~~
docker run ubuntu -v /home/data:/etc/var/app
~~~

# Start Command
>Used to start stopped containers
~~~
docker start <container id>
docker start <container name>
~~~
# Stop Command
>Used to stop running containers.
>Sends stop command to container and waits for 6 seconds for contariner to wrap up and stop, else sends ***kill command***
~~~
docker stop <container id>
docker stop <container name>
~~~
# Pause Command
>Pauses a running container as is.
~~~
docker pause <container id>
docker pause <container name>
~~~
# Kill Command
>Kills a running container immediately, does not wait for the container to finish up.
~~~
docker kill <container id>
docker kill <container name>
~~~
# List Containers
>Used to list all containers
~~~
docker ps
~~~
>To lists all containers includiong ***stopped*** containers, use:
~~~
docker ps -a
~~~

# EXEC command
>Executes a command in running container
~~~
docker exec <container id>  <command>
docker exec <container name> <command>
~~~