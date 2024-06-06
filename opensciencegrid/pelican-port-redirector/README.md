pelican-port-redirector
=======================

This image is meant to be run as a sidecar along a pelican-cache
container, to do an HTTP 301 permanent redirect to the pelican
cache port.  The goal is for Pelican cache deployments to maintain
compatibility with stash-cache deployments by listening on both ports
8000 and 8443.

The idea is based on https://github.com/morbz/docker-web-redirect

Usage
-----
The following environment variables are accepted:

-   `PELICAN_SERVER_HOSTNAME`: 
    The hostname to redirect to.  This should be the external FQDN
    of the cache.  If not specified, this is `localhost`.

-   `PELICAN_CACHE_PORT`:
    The port that the Pelican cache is listening on.
    If not specified, this is `8443`.

-   `LISTEN_PORT`:
    The port that incoming connections will arrive on.
    If not specified, this is `8000`.

