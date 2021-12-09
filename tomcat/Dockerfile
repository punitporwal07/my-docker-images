# Dockerfile for building tomcat image on centos, with few software as possible.
#
# Version  1.0
#
#
# pull base image of centos
FROM centos

MAINTAINER Punit <punitporwal07@gmail.com>

WORKDIR /software/tomcat

RUN echo "===> creating tomcat user & group..." && \
    useradd red && groupadd redgrp && \
    \
    \
    mkdir -p /software/tomcat && \
    \
    \
    echo "===> installing java.." && \
    \
    \
    yum -y install java && yum -y clean all

RUN curl -O https://www-eu.apache.org/dist/tomcat/tomcat-8/v8.5.41/bin/apache-tomcat-8.5.41.tar.gz && \
    \
    \
    tar -xvzf apache-tomcat-8.5.41.tar.gz && \
    \
    \
    chown -R red:redgrp /software/

EXPOSE 8000

CMD ["/software/tomcat/apache-tomcat-8.5.41/bin/./catalina.sh", "run"]

#ENTRYPOINT ["/software/tomcat/apache-tomcat-8.5.41/bin/startup.sh"]
#CMD /software/tomcat/apache-tomcat-8.5.41/bin/startup.sh
