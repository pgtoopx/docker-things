FROM phusion/baseimage:master

ENV MAVEN_VERSION 3.3.9
ENV MAVEN_HOME /usr/share/maven
ARG CHROME_DRIVER_VERSION=74.0.3729.6


# JAVA
RUN apt-get -y update
RUN apt install -y openjdk-8-jdk 

RUN mkdir -p /usr/share/maven \
  && curl -fsSL http://apache.osuosl.org/maven/maven-3/${MAVEN_VERSION}/binaries/apache-maven-${MAVEN_VERSION}-bin.tar.gz \
    | tar -xzC /usr/share/maven --strip-components=1 \
  && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn

COPY settings.xml /root/.m2
