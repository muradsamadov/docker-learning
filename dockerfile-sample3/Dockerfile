FROM centos

ARG user=application

RUN yum -y install httpd unzip

LABEL maintainer=murad
LABEL vendor=isb

ENV HTML beginner-html-site-styled

WORKDIR /var/www/html/

ADD https://github.com/mdn/$HTML/archive/gh-pages.zip ./code.zip

RUN unzip code.zip && mv $HTML-gh-pages/* . && echo $HTML > ./env.html

RUN useradd $user && chown $user:$user /var/www/html -R

USER $user

RUN rm -rf code.zip $HTML-gh-pages/

USER root

CMD apachectl -DFOREGROUND