FROM openjdk:8-alpine
LABEL maintainer=thej
WORKDIR /app
COPY build/docker/libs libs/
COPY build/docker/resources resources/
COPY build/docker/classes classes/
ENTRYPOINT ["java", "-Dspring.profiles.active=production", "-Xmx2048m", "-cp", "/app/resources:/app/classes:/app/libs/*", "eu.xword.labs.gc.JavaAppApplication"]
EXPOSE 8888 8888
