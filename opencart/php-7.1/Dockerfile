FROM php:7.1-apache
RUN apt -yqq update
RUN apt -yqq install libxml2-dev
RUN apt -yqq install zlib1g-dev
RUN apt -yqq install libpng-dev
RUN apt-get install -y libfreetype6-dev libjpeg62-turbo-dev
RUN docker-php-ext-install xml
RUN docker-php-ext-install zip
RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/  &&  \
            docker-php-ext-install gd
RUN apt-get install git -y
RUN git clone https://github.com/opencart/opencart.git /var/www/html/opencart
RUN find /var/www/html/ -type d -exec chmod 775 {} \;
RUN find /var/www/html/ -type f -exec chmod 664 {} \;
RUN chown -R www-data /var/www/html/

