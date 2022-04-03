FROM ubuntu:20.04

RUN apt-get update && \
        apt install -y default-jre && \
        apt install -y wget;

RUN mkdir /usr/local/tomcat
RUN wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.62/bin/apache-tomcat-9.0.62.tar.gz -O /tmp/tomcat.tar.gz
RUN cd /tmp && tar xvfz tomcat.tar.gz
RUN cp -Rv /tmp/apache-tomcat-9.0.62/* /usr/local/tomcat/

WORKDIR  /usr/local/tomcat/webapps/

COPY java-tomcat-maven-example.war ./

EXPOSE 8080

CMD /usr/local/tomcat/bin/catalina.sh run