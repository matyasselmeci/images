FROM docker.io/library/nginx:1.27.0-alpine

COPY default.conf.template /etc/nginx/templates/default.conf.template

# Do not override this env var
ENV NGINX_ENVSUBST_FILTER="LISTEN_PORT|PELICAN.*"

#
# The following are meant to be overridden:
#

ENV LISTEN_PORT=8000
ENV PELICAN_CACHE_PORT=8443
ENV PELICAN_SERVER_HOSTNAME=localhost
