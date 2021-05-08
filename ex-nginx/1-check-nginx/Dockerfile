FROM ubuntu:20.04

RUN apt-get update && apt-get install -y \
    vim \
    nginx \
    sudo \
    lsof
COPY ./deploy /etc/nginx/conf.d
COPY ./build /var/www/ex_nginx/build
