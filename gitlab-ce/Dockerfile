FROM gitlab/gitlab-ce:latest

COPY gitlab.key /etc/ssl/gitlab.key
COPY gitlab.crt /etc/ssl/gitlab.crt
COPY gitlab.crt /usr/local/share/ca-certificates/gitlab.crt
RUN update-ca-certificates
