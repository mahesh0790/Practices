FROM ubuntu
RUN apt-get update
RUN apt-get install -y tzdata
RUN dpkg-reconfigure -f noninteractive tzdata
RUN apt-get install -y php7.2 php7.2-mbstring php7.2-xml
RUN apt-get install -y sudo
RUN apt-get install -y curl
RUN curl -sS https://getcomposer.org/installer | php
RUN apt-get install -y composer
RUN apt-get install -y zip unzip 
WORKDIR /var/www/html
RUN rm -fr index.nginx-debian.html
RUN composer create-project --prefer-dist laravel/laravel laravel
RUN chown -R www-data:www-data laravel

