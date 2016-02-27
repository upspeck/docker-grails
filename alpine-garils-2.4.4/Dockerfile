FROM upspeck/java:alpine-java-.17
MAINTAINER Jeyson Maia <jeyson@upspeck.io>

RUN apk upgrade --update \
    && apk add --update unzip wget \

# Install Grails.
RUN cd /tmp \
    && wget -qO grails-2.4.4.zip \
       https://github.com/grails/grails-core/releases/download/v2.4.4/grails-2.4.4.zip \
    && unzip  grails-2.4.4.zip -d /opt \
    && mv /opt/grails-2.4.4 /opt/grails

# Define commonly used JAVA_HOME variable
ENV GRAILS_HOME /opt/grails
ENV GRAILS_HOME /opt/grails/bin

# Clean S.O

RUN rm -rf  /tmp/* /var/cache/apk/* \
            && apk del wget unzip
