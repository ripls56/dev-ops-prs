FROM ubuntu:latest
LABEL authors="ripls"

RUN apt-get update && apt-get install -y \
    x11-apps \
    xauth \
    openjdk-11-jre\
    && rm -rf /var/libs/apt/lists/*

COPY calc.jar .

ENV DISPLAY=:0
ENTRYPOINT ["java", "-jar", "calc.jar"]