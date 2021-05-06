FROM vindevoy/centos8-base:latest

LABEL maintainer = "Yves Vindevogel (vindevoy) - yves.vindevogel@asynchrone.com"

COPY resources/openresty.repo /etc/yum.repos.d/openresty.repo
COPY resources/openresty.sh /root/openresty.sh
COPY resources/openresty.conf /root/openresty.conf

RUN set -x && \ 
    dnf update -y --nodocs && \ 
    dnf install -y --nodocs openresty && \ 
    chmod +x /root/openresty.sh && \ 
    mkdir -p /var/log/openresty && \ 
    chmod 664 /var/log/openresty

EXPOSE 80

CMD ["/bin/bash", "-c", "/root/openresty.sh"]
