# Microservice Applications and It's Port Mapping
We will be creating a lot of microservices so please refer below ports mapping (microservice applications with their ports):

For the API-Gateway application, use the 9191 port.

For the Department-Service application, use the 8080 port and for its instance, use port 8082

For the Employee-Service application, use the 8081 port.

For the Config-Server application, use the 8888 port.

For the Service-Registry application, use the 8761 port.

For the Organization-Service application, use the 8083 port.

For the React-Frontend application, use the 3000 port.

Zipkin Server uses the default port 9411

Here is the screenshot image for your reference. Download and use it on your machine.

-----

### Update on Spring Boot 3 Version
This project supports the Latest Spring Boot 3 and Spring Cloud 2022.0.0.

So while creating Spring boot projects using https://start.spring.io/, you can choose the latest version of Spring Boot 3.0.x.

Conclusion:

This project supports both Spring Boot 2.x and Spring Boot 3.x users.

-----

Update on Using Spring Boot 3 Version
In the next lecture, make the below small change to support Spring Boot 3 and Spring Cloud 2022.0.0:

- Don’t annotate an entry-point DepartmentServiceApplication class with @EnableEurekaClient - This annotation was removed in spring cloud 2022.0.0 and provided auto-configuration.

- Don’t annotate an entry-point ApiGatewayApplication class with @EnableEurekaClient - This annotation was removed in spring cloud 2022.0.0 and provided auto-configuration.

- Don’t annotate an entry-point ConfigServerApplication class with @EnableEurekaClient - This annotation was removed in spring cloud 2022.0.0 and provided auto-configuration.

# Docker

## rabbitmq

- docker pull rabbitmq:3.11.0
- docker run --rm -it -p 5672:5672 rabbitmq:3.11.0
-----
## docker hub
- docker build -t springboot-docker-demo:0.1.RELEASE .
- docker run -p 8080:8080 springboot-docker-demo
- docker logs -f 143...
- docker login
- docket tag springboot-docker-demo htrix/springboot-docker-demo:0.1.RELEASE
- docker images
- docker push htrix/springboot-docker-demo:0.1.RELEASE
- docker pull htrix/springboot-docker-demo

## Mysql
- docker run -p 3307:3306 --name localhost -e MYSQL_ROOT_PASSWORD=sasa -e MYSQL_DATABASE=employee_db -e MYSQL_USER=htrix -e MYSQL_PASSWORD=sasa -d mysql:0.0.31
- docker exec -it localhost bash
- mysql -u root -p
- show databases
- 




