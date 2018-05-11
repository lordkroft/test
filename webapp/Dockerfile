FROM php:7.0-apache 
RUN apt-get update \
   && apt-get install -y apache2 mysql-client && rm -rf /var/lib/apt
RUN sed -i 's|/var/lib/mysql|/var/lib/mysql-data|g' /etc/mysql/my.cnf
WORKDIR /var/www/html
CMD ["apachectl", "-D", "FOREGROUND"]
EXPOSE 80

