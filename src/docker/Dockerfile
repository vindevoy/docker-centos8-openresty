###
#
#	Yves Vindevogel (vindevoy)
#	2021-05-05
#
#	Run a command line script and send the output in html via openresty
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

ENV PATH=/usr/local/openresty/nginx/sbin:$PATH

EXPOSE 80

#CMD ["/bin/bash"]
CMD ["/bin/bash", "-c", "/root/openresty.sh"]

