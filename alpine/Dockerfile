FROM nginx:mainline-alpine
MAINTAINER IF Fulcrum "fulcrum@ifsight.net"

RUN apk update && apk upgrade && deluser nginx && adduser -h /var/www/html -s /sbin/nologin -D -H -u 1971 nginx

ENTRYPOINT ["/usr/sbin/nginx"]
