FROM php:7.0-apache 
#tecadmin/ubuntu-ssh:16.04

RUN apt-get update \
   && apt-get install -y apache2 mysql-client && rm -rf /var/lib/apt
#COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf
#COPY index.html /var/www/html/
RUN sed -i 's|/var/lib/mysql|/var/lib/mysql-data|g' /etc/mysql/my.cnf
WORKDIR /var/www/html
CMD ["apachectl", "-D", "FOREGROUND"]
#CMD ["/usr/bin/supervisord"]
EXPOSE 80

