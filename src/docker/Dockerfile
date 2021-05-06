###
#
#	Yves Vindevogel (vindevoy)
#	2021-05-05
#
#	Hello world with OpenResty, the base for further CLI over HTTP(S)
#
###

FROM vindevoy/centos8-base:latest

LABEL maintainer = "Yves Vindevogel (vindevoy) - yves.vindevogel@asynchrone.com"

COPY resources/openresty.repo /etc/yum.repos.d/openresty.repo
COPY resources/openresty.sh /root/openresty.sh
COPY resources/openresty.conf /root/openresty.conf

RUN dnf update -y --nodocs
RUN dnf install -y --nodocs openresty

RUN chmod +x /root/openresty.sh 

RUN mkdir -p /var/log/openresty
RUN chmod 664 /var/log/openresty

EXPOSE 80

#CMD ["/bin/bash"]
CMD ["/bin/bash", "-c", "/root/openresty.sh"]

