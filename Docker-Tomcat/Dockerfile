FROM ubuntu:18.04
RUN apt-get -y update
RUN apt-get -y install openjdk-8-jdk wget
WORKDIR /usr/
RUN wget http://mirrors.estointernet.in/apache/tomcat/tomcat-9/v9.0.19/bin/apache-tomcat-9.0.19.tar.gz
RUN tar -zxvf apache-tomcat-9.0.19.tar.gz
RUN mv apache-tomcat-9.0.19 tomcat9
ENV CATALINA_HOME /usr/share/tomcat9
ENV CATALINA_BASE /usr/share/tomcat9/lib/tomcat9
ENV CATALINA_PID /usr/share/tomcat9/run/tomcat9.pid
ENV CATALINA_SH /usr/share/tomcat9/bin/catalina.sh
EXPOSE 8080
ENTRYPOINT [ "/usr/share/tomcat9/bin/catalina.sh", "run" , "daemon off;"]
