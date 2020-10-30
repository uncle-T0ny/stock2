[tags]: <> (docker, stats, info)

### view amount of images and containers
docker info

### view info about docker CPU/RAM consuming
docker stats

### view list of docker images
docker image ls

### view list of docker containers
docker container ls --all

### login to docker and tag an image
docker login
docker tag friendlyhello doitrant/get-started:part2

### pull and run docker image remotely
docker run -p 4000:80 doitrant/repository:tag

docker run --name mongo -d -p 27017:27017 mongo:4.0.17

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

### docker get latest logs
docker logs --tail 500 app-sender

### Copy a file from Docker container to host:
docker cp 72ca2488b353:/foo.txt foo.txt

### Copy a file from host to container: 
docker cp foo.txt 72ca2488b353:/foo.txt

### Investigate docker image
docker image history --no-trunc registry.mmdsmart.com/mmd/docker-base/sonar
docker run -it registry.mmdsmart.com/mmd/docker-base/sonar sh 
[tags-end]: <>
