FROM alpine

RUN apk update && \
    apk add --no-cache collectd supervisor

COPY collectd.conf /etc/collectd/

# Copy Docker Entrypoint
COPY docker-entrypoint.sh /
RUN chmod +x /docker-entrypoint.sh

ENTRYPOINT ["/docker-entrypoint.sh"]

COPY config/supervisord/*.ini /etc/supervisor.d/
