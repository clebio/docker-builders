FROM haproxy:latest
COPY haproxy.cfg /usr/local/etc/haproxy/haproxy.cfg

RUN mkdir /etc/ssl
COPY gitlab.pem /etc/ssl/gitlab.pem
