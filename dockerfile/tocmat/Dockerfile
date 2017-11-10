FROM ubuntu:17.10
ADD res/apache-tomcat-*.tar.gz /opt/tomcat
ADD res/server-jre-*.tar.gz /opt/java
WORKDIR /opt/tomcat
RUN ln -s apache-tomcat-* /opt/tomcat/latest
WORKDIR /opt/java
RUN ln -s jdk* /opt/java/latest
ENV JAVA_HOME=/opt/java/latest
ENV CATALINA_HOME=/opt/tomcat/latest
ENV PATH $CATALINA_HOME/bin:$PATH
EXPOSE 8080
CMD ["catalina.sh", "run"]