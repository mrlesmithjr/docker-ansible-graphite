FROM alpine-collectd

RUN apk update && \
    apk add --no-cache nginx

COPY config/supervisord/*.ini /etc/supervisor.d/
RUN mkdir /run/nginx

EXPOSE 80
