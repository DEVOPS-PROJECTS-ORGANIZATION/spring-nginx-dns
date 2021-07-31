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
