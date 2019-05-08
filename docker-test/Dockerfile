FROM centos:7<br>
MAINTAINER dock<br>

RUN yum install -y wget<br>

RUN cd /<br>

ADD jdk-8u211-linux-x64.tar.gz /<br>

RUN wget http://apache.stu.edu.tw/tomcat/tomcat-7/v7.0.94/bin/apache-tomcat-7.0.94.tar.gz<br>
RUN tar zxvf apache-tomcat-7.0.94.tar.gz<br>

ENV JAVA_HOME=/jdk1.8.0_211<br>
ENV PATH=$PATH:/jdk1.8.0_211/bin<br>
CMD ["/apache-tomcat-7.0.82/bin/catalina.sh", "run"]<br>
