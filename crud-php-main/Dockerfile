FROM php:8.3-apache

WORKDIR /var/www/php

COPY . /var/www/php

RUN echo "ServerName localhost"  >> /etc/apache2/apache2.conf



RUN apt-get update && apt-get upgrade -y && docker-php-ext-install mysqli pdo pdo_mysql
RUN docker-php-ext-enable mysqli pdo_mysql 


ENV MYSQL_HOST=db
ENV MYSQL_DATABASE=mydb
ENV MYSQL_ROOT_PASSWORD=root
ENV MYSQL_USER=user
ENV MYSQL_PASSWORD=pass
ENV MYSQL_PORT=3306

EXPOSE 80