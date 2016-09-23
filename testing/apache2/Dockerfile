FROM alpine-collectd

RUN apk update && \
    apk add --no-cache apache2

COPY config/supervisord/*.ini /etc/supervisor.d/
RUN mkdir /run/apache2

EXPOSE 80
