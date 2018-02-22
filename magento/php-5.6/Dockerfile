FROM php:5.6.33-apache
RUN apt -yqq update

## Libraries
RUN apt -yqq install libxml2-dev
RUN apt -yqq install zlib1g-dev
RUN apt -yqq install libpng-dev
RUN apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libmcrypt-dev libldap2-dev



## Dependencies
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install xml
RUN docker-php-ext-install zip
RUN docker-php-ext-install -j$(nproc) iconv mcrypt
RUN docker-php-ext-configure ldap --with-libdir=lib/x86_64-linux-gnu/ && \
    docker-php-ext-install ldap
RUN docker-php-ext-install soap


RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/  &&  \
            docker-php-ext-install gd

## GIT
RUN apt-get install git -y
RUN apt-get install vim -y
RUN a2enmod rewrite

## File create and permissions

RUN find /var/www/html/ -type d -exec chmod 775 {} \;
RUN find /var/www/html/ -type f -exec chmod 664 {} \;
RUN chown -R www-data:www-data /var/www/html/





