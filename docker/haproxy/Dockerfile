FROM haproxy:1.6.2

#MAINTAINER  eder.roger.souza@gmail.com

ENV REFRESHED_AT 2015-12-21

#RUN apt-get -y update

#RUN apt-get install -y haproxy

#RUN apt-get install -y socat

# Add files.
# ADD haproxy.cfg /etc/haproxy/haproxy.cfg
COPY haproxy.cfg /usr/local/etc/haproxy/haproxy.cfg
#WORKDIR /etc/haproxy

#CMD ["bash", "/haproxy-start"]

#EXPOSE 80
#EXPOSE 443
