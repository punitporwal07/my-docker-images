FROM fedora:20
MAINTAINER "Punit Porwal"

RUN yum -y update && yum clean all
RUN yum -y install httpd && yum clean all
RUN echo "Apache Instance 1.0 to test Ingress funcitonality" >> /var/www/html/index.html

EXPOSE 80

ADD run.sh /run.sh
RUN chmod -v +x /run.sh

CMD ["/run.sh"]
