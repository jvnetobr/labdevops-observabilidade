#FROM openjdk:8-jdk-alpine
FROM openjdk:23-jdk-bookworm

#RUN addgroup -S spring && adduser -S spring -G spring
RUN adduser spring

USER spring:spring

ARG JAR_FILE=target/*jar
COPY ${JAR_FILE} app.jar

#ENTRYPOINT ["java","-Xms128M","-Xmx128M","-XX:PermSize=64m","-XX:MaxPermSize=128m","-Dspring.profiles.active=prod","-jar","/app.jar"]
ENTRYPOINT ["java","-Xms128M","-Xmx128M","-Dspring.profiles.active=prod","-jar","/app.jar"]