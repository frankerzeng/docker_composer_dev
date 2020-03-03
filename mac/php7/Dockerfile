FROM  php:7.1.0-fpm

RUN pecl install swoole

RUN apt-get update && apt-get install -y vim
RUN apt-get install -y wget

RUN wget https://mirrors.aliyun.com/composer/composer.phar -O /usr/local/bin/composer 

RUN chmod a+x /usr/local/bin/composer
RUN export PATH=$PATH:/usr/local/php/bin

RUN composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/

RUN apt-get install zip unzip

