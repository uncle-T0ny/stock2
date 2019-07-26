[tags]: <> (docker)

### view amount of images and containers
docker info

### view list of docker images
docker image ls

### view list of docker containers
docker container ls --all

### login to docker and tag an image
docker login
docker tag friendlyhello doitrant/get-started:part2

### pull and run docker image remotely
docker run -p 4000:80 doitrant/repository:tag

### init swarm
docker swarm init

### run service with containers on the one host
docker stack deploy -c docker-compose.yml getstartedlab

### get service id
docker service ls

### list the tasks of the service
docker service ps getstartedlab_web

### down the stack
docker stack rm getstartedlab

### down the swarm
docker swarm leave --force

### stop all the containers
docker stop $(docker ps -aq)

### docker compose remove all images
docker-compose down --rmi=all

### build docker image with dockerfile
docker build - < docker/Dockerfile.local

### get docker free space
docker system df

### docker restart comnainer 
docker restart container_name

### docker remove all containers and all unused images
docker system prune -a

[tags-end]: <>
