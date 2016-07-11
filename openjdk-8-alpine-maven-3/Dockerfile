# OpenJDK 8
# Alpine Linux 
# Maven
# $ docker build . -t sabinthomas/openjdk-8-alpine-maven-3
 
FROM java:openjdk-8-alpine

MAINTAINER sabinthomas
LABEL version="1.0"
LABEL description="Alpine based JDK8 image with Maven"

RUN apk update
RUN MAVEN_VERSION=3.3.9 && \
    wget http://www-us.apache.org/dist/maven/maven-3/$MAVEN_VERSION/binaries/apache-maven-$MAVEN_VERSION-bin.tar.gz && \
    tar xzvf apache-maven-$MAVEN_VERSION-bin.tar.gz && mv apache-maven-$MAVEN_VERSION maven && \
    rm -f apache-maven-$MAVEN_VERSION-bin.tar.gz
ENV PATH=${PATH}:/maven/bin

EXPOSE 8080

