FROM openjdk:19-jdk-alpine3.16

ENV CATALINA_HOME /opt/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH

RUN mkdir -p /opt/tomcat
WORKDIR $CATALINA_HOME

RUN apk update
RUN apk add vim wget zip gettext

ENV TOMCAT_VERSION 9.0.75
COPY apache-tomcat-9.0.75.tar.gz .


RUN tar -xf apache-tomcat-9.0.75.tar.gz
RUN mv apache-tomcat-9.0.75/* /opt/tomcat/
RUN rm -rf apache-tomcat-9.0.75.tar.gz tomcat

EXPOSE 8080
CMD ["catalina.sh","run"]
