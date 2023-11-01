##########Another way of Docker file###########
FROM openjdk:17-jdk-alpine
EXPOSE 8080
ARG JAR_FILE=build/libs/*.jar
COPY ${JAR_FILE} app/build/libs/
ENTRYPOINT ["java", "-jar", "/app/build/libs/demo-application-0.0.1-SNAPSHOT.jar"]
