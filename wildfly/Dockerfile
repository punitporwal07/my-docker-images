# this fedora image is of 75 MB
FROM fedora:24

MAINTAINER Punit <punitporwal07@gmail.com>

ENV WILDFLY_VERSION 9.0.2.Final

# Install necessary packages
RUN dnf -y install java-1.8.0-openjdk-devel tar && dnf clean all

RUN mkdir -p /software/jboss/wildfly

#Add Wildfly 9.0.2 to this image
RUN cd /tmp \
  && curl -O https://download.jboss.org/wildfly/$WILDFLY_VERSION/wildfly-$WILDFLY_VERSION.tar.gz \
      && tar xf wildfly-$WILDFLY_VERSION.tar.gz \
      && mv /tmp/wildfly-$WILDFLY_VERSION /software/jboss/wildfly \
      && rm /tmp/wildfly-$WILDFLY_VERSION.tar.gz
      
# Expose the ports we're interested in
EXPOSE 8080

# Set the default command to run on boot
# This will boot WildFly in the standalone mode and bind to all interface
CMD ["/software/jboss/wildfly/bin/standalone.sh", "-b", "0.0.0.0"]
