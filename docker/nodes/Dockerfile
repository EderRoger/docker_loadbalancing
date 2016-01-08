FROM ubuntu:14.04

MAINTAINER eder.roger.souza@gmail.com

ENV REFRESHED_AT 2015-12-21

RUN apt-get -y update

RUN apt-get install -y git

RUN apt-get install -y nginx

RUN mkdir -p /var/www/html/website

ADD ./global.conf /etc/nginx/conf.d/
ADD ./nginx.conf /etc/nginx/nginx.conf

WORKDIR /var/www/html/website

RUN git clone https://github.com/jweissig/episode-47

VOLUME [ "/var/log/nginx" ]

ENTRYPOINT ["/usr/sbin/nginx", "-g", "daemon off;"]

EXPOSE 80
