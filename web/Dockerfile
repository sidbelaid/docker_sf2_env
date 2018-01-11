FROM php:7.1-apache

RUN apt-get -y update

# Tools
RUN	apt-get install -y vim wget
RUN apt-get update -y
RUN	apt-get install -y git subversion
RUN	apt-get install -y zip unzip
RUN apt-get update -y
RUN	apt-get install -y imagemagick
RUN	apt-get install -y zlib1g-dev libicu-dev g++

# PHP extensions
RUN apt-get update -y
RUN	apt-get install -y libpng-dev
RUN	docker-php-ext-install gd
RUN	docker-php-ext-install pdo 
RUN	docker-php-ext-install pdo_mysql 
RUN	docker-php-ext-install intl
RUN	docker-php-ext-install opcache
RUN	docker-php-ext-install zip
RUN pecl install apcu \
  && docker-php-ext-enable apcu
  
# composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer 

# NodeJs et GruntJs
RUN apt-get update -y
RUN curl -sL https://deb.nodesource.com/setup_9.x | bash -
RUN	apt-get install -y nodejs
RUN	npm install -g grunt-cli

#install Imagemagick & PHP Imagick ext
RUN apt-get update && apt-get install -y \
        libmagickwand-dev --no-install-recommends
RUN pecl install imagick && docker-php-ext-enable imagick