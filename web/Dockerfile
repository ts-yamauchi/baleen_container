FROM php:7.0.8-apache

ADD composer.phar /usr/local/bin/composer

RUN apt-get update
RUN apt-get -y install \
	libicu-dev \
	zlib1g-dev
RUN docker-php-ext-install \
	intl \
	pdo \
	pdo_mysql \
	tokenizer \
	zip

# mod_rewriteを有効にする
RUN a2enmod rewrite