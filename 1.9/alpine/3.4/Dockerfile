FROM nginx:1.9-alpine
MAINTAINER IF Fulcrum "fulcrum@ifsight.net"

RUN echo "Cache bust 201606232004" && \
    apk update && apk upgrade

ENTRYPOINT ["/usr/sbin/nginx"]
