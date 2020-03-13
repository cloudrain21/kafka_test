FROM centos:latest
MAINTAINER Rain.i <cloudrain21@gmail.com>

RUN yum -y update
RUN yum -y install java-1.8.0-openjdk

RUN yum -y install wget
RUN wget http://apache.mirror.cdnetworks.com/zookeeper/stable/apache-zookeeper-3.5.7-bin.tar.gz

RUN mv apache-zookeeper-3.5.7-bin.tar.gz /usr/local
RUN cd /usr/local; tar zxf /usr/local/apache-zookeeper-3.5.7-bin.tar.gz
RUN cd /usr/local; ln -s apache-zookeeper-3.5.7-bin zookeeper

RUN mkdir -p /data
RUN echo 1 > /data/myid

RUN echo "tickTime=2000"   >  /usr/local/zookeeper/conf/zoo.cfg
RUN echo "initLimit=10"    >> /usr/local/zookeeper/conf/zoo.cfg
RUN echo "syncLimit=5"     >> /usr/local/zookeeper/conf/zoo.cfg
RUN echo "dataDir=/data"   >> /usr/local/zookeeper/conf/zoo.cfg
RUN echo "clientPort=2181" >> /usr/local/zookeeper/conf/zoo.cfg
RUN echo "server.1=zk001:2888:3888" >> /usr/local/zookeeper/conf/zoo.cfg

#ENTRYPOINT ["/usr/local/zookeeper/bin/zkServer.sh", "start"]
EXPOSE 2181    
