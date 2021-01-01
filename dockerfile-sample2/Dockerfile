FROM ubuntu:latest

MAINTAINER Samadov Murad <muradsamadov5@gmail.com>

RUN apt-get update -y
RUN apt-get install nginx -y

ADD [ "index.html", "/var/www/html/" ]

EXPOSE 80

ENTRYPOINT nginx -g 'daemon off;'