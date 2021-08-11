# Repository Summary
* Docker  
* Docker Compose
* Microservices-architecture (Spring Boot - Java Framework)
* Platform-Provided Service Discovery (Deployment infrastructure take care of service discovery)
* Service-discovery (Docker-DNS)
* API-gateway (NGINX)
# Microservices Demo

Restaurant application implemented in spring boot framework. NGINX is used as
API Gateway and Docker DNS service as service discovery.

In order to set up infrastructure run the following command:
```shell
docker-compose up --build
```

Application testing is available via `web_requests.sh` script.
```shell
web_requests.sh
```
In order to destroy infrastructure run the following command:
```shell
docker-compose down -v
```
# spring-nginx-dns Instructions
**Start Docker Daemon:** If you're using Docker for Windows, Then simply start the desktop app installed in:
```shell
C:\Program Files\Docker\Docker\Docker Desktop.exe
```
Position yourself using **Git Bash** in the folder where `docker-compose.yml` file is:
```
cd DOCKER-COMPOSE_FILE_PATH
```
Mapping environment variables from the environment file to the docker-compose.yml file (Check how your docker-compose.yml will finally look like, after environment variables substitution)
```shell
docker-compose --env-file .env config
```
To set up infrastructure run the following command in **Git Bash**:
```shell
docker-compose up --build
```
Docker-compose services/containers listing (one service one container)
```shell
docker-compose ps
```
```shell
docker ps
```
Request:
```GET http://localhost:8080/api/consumer/hello```  
```
http://localhost:8080/api/consumer/hello
```
Response:
```
Hello from consumer service with ip address 172.18.0.3!
```
Request:
```GET http://localhost:8080/api/kitchen/hello```  
```
http://localhost:8080/api/kitchen/hello
```
Response:
```
Hello from kitchen service with ip address 172.18.0.4!
```
Request:
```GET http://localhost:8080/api/order/hello```  
```
http://localhost:8080/api/order/hello
```
Response:
```
Hello from order service with ip address 172.18.0.2!
```
To destroy infrastructure run the following command in **Git Bash**:
```shell
docker-compose down -v
```
