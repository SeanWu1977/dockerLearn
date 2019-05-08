FROM centos:7
MAINTAINER dock

RUN yum install -y wget

RUN cd /

ADD jdk-8u211-linux-x64.tar.gz /

RUN wget http://apache.stu.edu.tw/tomcat/tomcat-7/v7.0.94/bin/apache-tomcat-7.0.94.tar.gz
RUN tar zxvf apache-tomcat-7.0.94.tar.gz

ENV JAVA_HOME=/jdk1.8.0_211
ENV PATH=$PATH:/jdk1.8.0_211/bin
CMD ["/apache-tomcat-7.0.94/bin/catalina.sh", "run"]
