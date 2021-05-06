###
#
#	Yves Vindevogel (vindevoy)
#	2021-05-05
#
#	Run a command line script and send the output in html via nginx
#
###

FROM vindevoy/centos8-base:latest

LABEL maintainer = "Yves Vindevogel (vindevoy) - yves.vindevogel@asynchrone.com"

RUN dnf install -y --nodocs nginx 

EXPOSE 80

CMD ["/usr/sbin/nginx", "-g", "daemon off;"]

