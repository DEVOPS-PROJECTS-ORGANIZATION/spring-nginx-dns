# Repository Summary

# Microservices Demo

Restaurant application implemented in spring boot framework. NGINX is used as
API Gateway and Docker DNS service as service discovery.

In order to set up infrastructure run the following command:
```
docker-compose up --build
```

Application testing is available via `web_requests.sh` script.
```
web_requests.sh
```
In order to destroy infrastructure run the following command:
```
docker-compose down -v
```
# spring-nginx-dns Instructions
**Start Docker Daemon:** If you're using Docker for Windows, Then simply start the desktop app installed in:
```
C:\Program Files\Docker\Docker\Docker Desktop.exe
```
Position yourself using **Command Line Interface (CLI)** in the folder where `docker-compose.yml` file is:
```
cd DOCKER-COMPOSE_FILE_PATH
```
Mapping environment variables from the environment file to the docker-compose.yml file (Check how your docker-compose.yml will finally look like, after environment variables substitution)
```
docker-compose --env-file .env config
```
