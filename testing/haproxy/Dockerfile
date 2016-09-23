FROM mrlesmithjr/haproxy

# Copy docker-gen files
COPY docker-gen/ /app/

# Copy Ansible playbook to do configurations
COPY haproxy.yml /

# Execute Ansible playbook
RUN ansible-playbook -i "localhost," -c local /haproxy.yml

ENV DOCKER_HOST unix:///tmp/docker.sock

ENV APACHE_BACKEND="apache" \
    APACHE_FRONTEND_PORT="8000" \
    BALANCE="roundrobin" \
    NGINX_BACKEND="nginx" \
    NGINX_FRONTEND_PORT="8001"

EXPOSE 8000 8001 9090

ENTRYPOINT ["/app/docker-entrypoint.sh"]

CMD ["docker-gen", "-config", "/app/docker-gen.cfg"]
