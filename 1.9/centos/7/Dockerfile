FROM fulcrum/centos
MAINTAINER IF Fulcrum "fulcrum@ifsight.net"

RUN echo "Cache bust 201604291406" && \
    groupadd -g 1971 nginx && useradd -d /var/lib/nginx -g nginx -M -n -s /sbin/nologin -u 1971 nginx && \
    yum --noplugins install -y http://dl.fedoraproject.org/pub/epel/7/x86_64/e/epel-release-7-7.noarch.rpm && \
    yum --noplugins install -y nginx && \
    yum --noplugins upgrade -y && \
    package-cleanup --dupes && \
    package-cleanup --cleandupes && \
    yum clean all

# expose the port
EXPOSE 80

ENTRYPOINT ["/usr/sbin/nginx"]
