FROM	debian:bullseye

RUN 	apt update && apt install -y nginx openssl vim curl

RUN	mkdir -p /etc/nginx/ssl \
	&& openssl req -x509 -nodes -days 365 -newkey rsa:2048 \
    	-out /etc/nginx/ssl/inception.crt \
    	-keyout /etc/nginx/ssl/inception.key \
    	-subj "/C=FR/ST=IDF/L=Paris/O=42/OU=42/CN=tebandam.42.fr/UID=tebandam"

RUN	mkdir -p /var/run/nginx

COPY	conf/nginx.conf /etc/nginx/nginx.conf

EXPOSE	443

CMD	["nginx", "-g", "daemon off;"]
