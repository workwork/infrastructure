FROM jwilder/docker-gen

# File Author / Maintainer
MAINTAINER Work-Work AS

# VOLUME ["/var/run/docker.sock:/var/run/docker.sock"]
# COPY /var/run/docker.sock /tmp/docker.sock
COPY ./nginx.tmpl /etc/docker-gen/templates/nginx.tmpl


ENTRYPOINT ["/usr/local/bin/docker-gen", "-notify-sighup", "nginx", "-watch", "-only-exposed", "-wait", "5s:30s", "/etc/docker-gen/templates/nginx.tmpl", "/etc/nginx/conf.d/default.conf"]

