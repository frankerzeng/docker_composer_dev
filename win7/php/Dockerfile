FROM php:5.6-fpm
RUN apt-get update 
RUN apt-get install -y wget
RUN apt-get install -y apt-transport-https 
RUN apt-get install -y graphviz libfreetype6-dev libjpeg62-turbo-dev libpng-dev libxml2-dev vim
RUN apt-get install -y libxml2-dev mcrypt
RUN apt-get install -y graphviz
RUN apt-get install -y libmcrypt-dev libreadline-dev
RUN apt-get install -y libmagick-dev


# php拓展
RUN docker-php-ext-install gd zip
RUN docker-php-ext-install bcmath pdo_mysql soap 
RUN docker-php-ext-install mcrypt
RUN docker-php-ext-install shmop
RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/
RUN pecl install memcache && docker-php-ext-enable memcache

#Install the xhprof extension 
ADD ./extend/xhprof-0.9.4 /tmp/xhprof 
RUN cd /tmp \
&& ( \
    cd xhprof/extension \
    && phpize \
    && ./configure \
    && make \
    && make install \
)
#&& rm -r xhprof \
#COPY ./xhprof.ini /usr/local/etc/php/conf.d/xhprof.ini
