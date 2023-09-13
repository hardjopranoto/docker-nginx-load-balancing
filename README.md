# Docker Nginx Load Balancing
Use Nginx with multiple Node.js web server to try load balancing in Docker

## Project Structure
The project structure of the repo.
```
.
|____web
| |____Dockerfile
| |____package.json
| |____server.js
|____lb
| |____Dockerfile
| |____nginx.conf
|____docker-compose.yml
```

## Build
Build up the service.
```
$ docker-compose up --build
```

## Hello Nginx
You can test the load balancing of nginx by rin the below cmd.
```
$ curl -i http://localhost:8888/
```
