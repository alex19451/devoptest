FROM tomcat:9.0-jre8-alpine

WORKDIR /usr/local/tomcat/webapps/

COPY /home/alex1945/repo/target/*.war .

CMD ["catalina.sh", "run"]