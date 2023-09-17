# Docker Nginx Load Balancing
Use Nginx to load balance 2 web server running Nginx in Docker. 

## Prerequisite
A Linux virtual machine running docker services. 
For the installation instructions, please refer to the following Docker Docs. 
https://docs.docker.com/engine/install/

You will then need to clone this repository. 
```
$ git clone https://github.com/hardjopranoto/nginx-lb
```

## Project Structure
The project structure of the repo.
```
.
|____web
| |____Dockerfile
|____lb
| |____Dockerfile
| |____nginx.conf
|____docker-compose.yml
```


## Build
Build up the service.
```
$ docker compose up -d
```

## Validate
Validate that the nodes are up and running.
```
$ docker compose ps
```

## Test
You can test the load balancing of nginx by running the command below.
```
$ curl -i http://localhost:8080/
```
The curl response should show the response load balance between web1 and web2. 

## Terminate
You can stop and terminate the containers by running the command below.
```
$ docker compose stop
$ docker compose down
$ docker rmi $(docker images -a -q)
```