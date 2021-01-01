FROM ubuntu:latest

#WORKDIR /opt

#COPY index.html index.html

EXPOSE 8080

RUN apt-get update -y ; apt-get install apt-utils net-tools iputils-ping -y

ADD [ "index.html", "/opt/" ]

ENTRYPOINT [ "ping" ]
CMD [ "8.8.8.8" ]