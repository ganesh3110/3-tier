FROM centos:7

LABEL Devops ="Ganesh"

USER root

WORKDIR /opt

ADD https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.99/bin/apache-tomcat-8.5.99.tar.gz .

RUN tar -xvzf /opt/apache-tomcat-8.5.99.tar.gz 

RUN yum install java-11-openjdk-devel -y

WORKDIR /opt/apache-tomcat-8.5.99/

COPY student.war webapps/student.war

ADD context.xml conf/context.xml

ADD https://s3-us-west-2.amazonaws.com/studentapi-cit/mysql-connector.jar lib/mysql-connector.jar

EXPOSE 8080

CMD ["/opt/apache-tomcat-8.5.99/bin/catalina.sh", "run"]


 




