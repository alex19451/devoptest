FROM maven:3.5.2-jdk-8-alpine

RUN apk update && \
    apk add git

WORKDIR /tmp/project

RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello ./

CMD mvn package