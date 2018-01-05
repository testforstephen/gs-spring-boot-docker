FROM openjdk:8-jdk-alpine
VOLUME /tmp
ARG JAR_FILE
ADD target/gs-spring-boot-docker-0.1.0.jar target/app.jar
EXPOSE 1044 8080
ENTRYPOINT exec java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -agentlib:jdwp=transport=dt_socket,server=y,suspend=y,address=1044,quiet=y -jar target/app.jar
