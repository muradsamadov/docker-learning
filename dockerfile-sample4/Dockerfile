FROM centos

RUN \
  yum -y install \
  httpd \
  mod_ssl \
  net-tools

COPY ./vhost.conf /etc/httpd/conf.d/

RUN mkdir /var/www/html/test.local

COPY ./test.local/* /var/www/html/test.local/

COPY ./localhost.crt /etc/pki/tls/certs/localhost.crt

COPY ./localhost.key /etc/pki/tls/private/localhost.key

#RUN mv /etc/httpd/conf.d/ssl.conf /etc/httpd/conf.d/ssl.conf.bck

CMD apachectl -DFOREGROUND