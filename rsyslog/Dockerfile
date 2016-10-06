FROM debian:latest

RUN apt-get update && apt-get install -y \
    rsyslog

RUN ln -sf /dev/stdout /var/log/syslog
COPY rsyslog.conf /etc/

CMD ["/usr/sbin/rsyslogd", "-n"]
