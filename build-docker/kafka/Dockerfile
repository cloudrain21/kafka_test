FROM centos:latest
MAINTAINER Rain.i <cloudrain21@gmail.com>

RUN yum -y update
RUN yum -y install java-1.8.0-openjdk
RUN yum -y install wget

RUN cd /usr/local; wget http://apache.mirror.cdnetworks.com/kafka/2.4.0/kafka_2.13-2.4.0.tgz
RUN cd /usr/local; tar xzf kafka_2.13-2.4.0.tgz
RUN cd /usr/local; ln -s kafka_2.13-2.4.0 kafka

RUN mkdir -p /data1
RUN mkdir -p /data2

# need modify /etc/hosts file for zookeeper
# need modify config file

EXPOSE 9092    
