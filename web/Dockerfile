FROM php:7.1-apache

RUN apt-get -y update
RUN	apt-get install -y zlib1g-dev libicu-dev g++ git zip unzip ImageMagick
RUN	docker-php-ext-install pdo 
RUN	docker-php-ext-install pdo_mysql 
RUN	docker-php-ext-install intl 
#RUN	docker-php-ext-install curl 
#RUN	docker-php-ext-install imap 
RUN	docker-php-ext-install opcache
#RUN	docker-php-ext-install xml 
#RUN	docker-php-ext-install soap
RUN	docker-php-ext-install zip
	
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer 
