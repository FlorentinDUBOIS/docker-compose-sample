FROM alpine:latest

RUN apk add --no-cache openssh-client bash git tar curl
RUN curl https://getcaddy.com | bash -s http.cors,http.git

COPY Caddyfile /etc/Caddyfile

EXPOSE 80 443 2015
VOLUME /srv/http

ENTRYPOINT ["/usr/local/bin/caddy"]
CMD ["--conf", "/etc/Caddyfile"]
