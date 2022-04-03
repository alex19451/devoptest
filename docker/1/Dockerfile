FROM ubuntu:20.04

ARG project='https://github.com/boxfuse/boxfuse-sample-java-war-hello'
ARG dir_name='java-test'


WORKDIR /home/


RUN apt-get update && \
        apt install -y default-jre && \
        apt install -y maven && \
        apt install -y wget && \
        apt install -y git;

RUN mkdir /usr/local/tomcat
RUN wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.62/bin/apache-tomcat-9.0.62.tar.gz -O /tmp/tomcat.tar.gz
RUN cd /tmp && tar xvfz tomcat.tar.gz
RUN cp -Rv /tmp/apache-tomcat-9.0.62/* /usr/local/tomcat/


RUN git clone $project $dir_name && \
        cd $dir_name && \
        mvn package && \
        cd /home/$dir_name/target && \
        cp *.war /usr/local/tomcat/webapps/;

EXPOSE 8080

CMD /usr/local/tomcat/bin/catalina.sh run