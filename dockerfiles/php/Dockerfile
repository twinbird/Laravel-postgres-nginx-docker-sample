FROM php:7.3-fpm-alpine
RUN apk --update add \
	&& apk add build-base curl zip unzip 
RUN cd /usr/bin && curl -sS https://getcomposer.org/installer | php && ln -f -s /usr/bin/composer.phar /usr/bin/composer
RUN apk add --update libxml2-dev curl-dev postgresql-dev $PHPIZE_DEPS
RUN pecl install xdebug
RUN docker-php-ext-install pdo_pgsql mbstring xml curl session tokenizer json
RUN docker-php-ext-enable pdo_pgsql mbstring xml curl session tokenizer json xdebug
WORKDIR /var/www/html
