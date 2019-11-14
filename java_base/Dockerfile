FROM centos7base2:latest
ADD jdk-8u211-linux-x64.tar.gz /usr/local/
ENV JAVA_HOME=/usr/local/jdk1.8.0_211 \
 JRE_HOME=/usr/local/jdk1.8.0_211/jre \
 CLASSPATH=.:/usr/local/jdk1.8.0_211/lib:/usr/local/jdk1.8.0_211/lib
ENV PATH $PATH:$JAVA_HOME/bin
