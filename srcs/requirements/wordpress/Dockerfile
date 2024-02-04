FROM debian:bullseye

RUN apt update && apt install -y \
	curl \
	php-mysql \
	php-mysqli \
	mariadb-client \
	php \
	php-fpm && \
	mkdir -p /run/php

RUN curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar && \
	chmod +x wp-cli.phar && \
	mv wp-cli.phar /usr/local/bin/wp

COPY ./conf/www.conf /etc/php/7.4/fpm/pool.d/

COPY ./tools/script.sh /

RUN chmod +x script.sh

CMD ["/script.sh"]
