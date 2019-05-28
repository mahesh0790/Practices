FROM ubuntu:18.04
RUN apt-get update
RUN apt-get install -y apache2
ENTRYPOINT ["apache2ctl" , "-D" , "FOREGROUND"]
EXPOSE 80
