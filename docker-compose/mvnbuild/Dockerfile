FROM ubuntu:20.04

RUN apt-get update && \
    apt install -y maven && \
    apt install -y git;

WORKDIR /tmp/project

RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello ./

RUN mvn package