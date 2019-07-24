FROM phusion/baseimage:master


ENV JAVA_HOME /usr/lib/jvm/java-8
ENV MAVEN_VERSION 3.3.9
ENV MAVEN_HOME /usr/share/maven
ARG CHROME_DRIVER_VERSION=74.0.3729.6


# JAVA
RUN apt-get -y update
RUN apt -y install tar
COPY jdk-8u221-linux-x64.tar.gz /tmp
RUN  tar -zxvf jdk-8u221-linux-x64.tar.gz
RUN mv jdk1.8.0_221/ ${JAVA_HOME}
RUN echo export JAVA_HOME=${JAVA_HOME} >> ~/.bash_profile && echo export PATH=\$PATH:$JAVA_HOME/bin >> ~/.bash_profile && source ~/.bash_profile
RUN java -version