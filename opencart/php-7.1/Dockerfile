FROM php:7.1-apache
RUN apt-get update 
RUN apt-get upgrade -y &&\
    apt-get install vim -y
RUN apt-get install git -y
RUN git clone https://github.com/opencart/opencart.git /var/www/html/opencart
RUN find /var/www/html/ -type d -exec chmod 775 {} \;
RUN find /var/www/html/ -type f -exec chmod 664 {} \;
RUN chown -R www-data /var/www/html/

 
