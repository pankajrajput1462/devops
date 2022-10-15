
# Devops Commands

# Docker

List of images: `$ docker images`

> Container statics and details in terminal:
 
 `$ docker stats`

To expose just one port, this is what you need to do: `$ docker run -p <host_port>:<container_port>`

To expose multiple ports, simply provide multiple -p arguments:
`$ docker run -p <host_port1>:<container_port1> -p <host_port2>:<container_port2>`

In case you would like to expose a range of continuous ports, you can run docker like this:
 `docker run -it -p 7100-7120:7100-7120/tcp `

Eg. `$ docker run -p 3001:3000 -p 23:22`

List running docker process: `$ docker ps`

 To remove all <none name images>
 
 `$ docker images -f "dangling=true"  -q`
 
Before performing the removal command, you can get a list of all non-running (stopped) containers that will be removed using the following command:
`docker container ls -a --filter status=exited --filter status=created`

For remove: all stopped containers, all networks not used by at least one container, all dangling images, all build cache

`$ sudo docker system prune`

List of all active and inactive container
`$ docker container ls -a`

Run container eg. my sql docker image

`sudo docker container run -d  {ImageId} --env="MYSQL_ROOT_PASSWORD=root"`

For removing container:
`$ docker container rm <container_Id 1> <container_id2>`

Remove containers using filters
`$ docker container prune --filter "until=12h"`

To stop all running containers use the docker container stop command followed by a list of all containers IDs.
`$ docker container stop $(docker container ls -aq)`

Once all containers are stopped you can remove them using the docker container stop command followed by the containers ID list.
`$ docker container rm $(docker container ls -aq)`

> Removing Docker Images

For finding images:
`$ docker image ls`

For remove image: 
`$ docker image rm <ImageId_1>  <ImageId_2>`

> Remove dangling images

`$ docker image prune`

Remove all unused images

`$ docker image prune -a`

Remove images using filters

`$ docker image prune -a --filter "until=12h"`

> Removing Docker Volumes

First find the list of docker volume

`$ docker volume ls`

Remove volume:
`$ docker volume rm 4e12af8913af888ba67243dec78419bf18adddc3c7a4b2345754b6db64293163`

Remove all unused volumes:
`$ docker volume prune`

> Removing Docker Networks

Find the network:
`$ docker network ls`

Remove the network:
`$ docker network rm <Network Name>`

open container:
`$ sudo docker exec -it <ContainerId> sh`

>Important URL - 
 - [https://stackoverflow.com/questions/34004076/difference-between-docker-registry-and-repository](https://link) 
 - [https://stackoverflow.com/questions/23735149/what-is-the-difference-between-a-docker-image-and-a-container](https://link)
 - [https://stackoverflow.com/questions/31115098/in-docker-what-is-the-difference-between-an-image-and-a-repository](https://link)

