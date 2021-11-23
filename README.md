# SpringBoot-Docker-Example

Tutorial link: https://spring.io/guides/gs/spring-boot-docker/

# Command lines

Build a Docker Image with Gradle
You can build a tagged docker image with Gradle in one command:

./gradlew bootBuildImage --imageName=springio/gs-spring-boot-docker

Build a Docker Image with Maven
To get started quickly, you can run the Spring Boot image generator without even changing your pom.xml 
(remember that the Dockerfile, if it is still, there is ignored):

./mvnw spring-boot:build-image -Dspring-boot.build-image.imageName=springio/gs-spring-boot-docker

sudo docker run -p 8080:8080 -t springio/gs-spring-boot-docker

or

using spring profiles

docker run -e "SPRING_PROFILES_ACTIVE=prod" -p 8080:8080 -t springio/gs-spring-boot-docker