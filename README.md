# docker-learning
## Usage
### Build
```
docker build -t <image_name> .
```
### Run
```
docker run -it --rm <image_name>
```
### Push
```
docker login
docker tag <image_name> <docker_hub_username>/<image_name>
docker push <docker_hub_username>/<image_name>
```
### Pull
```
docker pull <docker_hub_username>/<image_name>
```
### Remove
```
docker rmi <image_name>
```
### Remove all images
```
docker rmi $(docker images -q)
```
### Remove all containers
```
docker rm $(docker ps -a -q)
```
### Remove all images and containers
```
docker rmi $(docker images -q) && docker rm $(docker ps -a -q)
```
### Remove all images and containers and volumes
```
docker rmi $(docker images -q) && docker rm $(docker ps -a -q) && docker volume rm $(docker volume ls -q)
```
### Remove all images and containers and volumes and networks
```
docker rmi $(docker images -q) && docker rm $(docker ps -a -q) && docker volume rm $(docker volume ls -q) && docker network rm $(docker network ls -q)
```