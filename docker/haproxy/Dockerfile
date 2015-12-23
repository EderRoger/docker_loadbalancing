FROM ubuntu:14.04

MAINTAINER  eder.roger.souza@gmail.com

ENV REFRESHED_AT 2015-12-21

RUN apt-get -y update

RUN apt-get install -y libssl1.0.0 libpcre3 --no-install-recommends

RUN apt-get install -y haproxy

RUN apt-get install -y socat

# Define mountable directories.
VOLUME ["/haproxy-override"]

# Add files.
ADD haproxy.cfg /etc/haproxy/haproxy.cfg
ADD start.bash /haproxy-start

RUN sed -i 's/^ENABLED=.*/ENABLED=1/' /etc/default/haproxy

WORKDIR /etc/haproxy

CMD ["bash", "/haproxy-start"]

EXPOSE 80
EXPOSE 443
