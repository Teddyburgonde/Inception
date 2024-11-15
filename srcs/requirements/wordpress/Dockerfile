FROM debian:bullseye

RUN apt update && apt install -y php7.4 php7.4-fpm php7.4-mysql mariadb-client wget curl vim unzip

RUN mkdir -p /run/php

EXPOSE 9000

CMD ["php-fpm7.4", "-F"]
