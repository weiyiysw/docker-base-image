FROM centos7sup:latest
ADD filebeat-7.4.2-linux-x86_64.tar.gz /usr
RUN ln -s /usr/filebeat-7.4.2-linux-x86_64 /usr/filebeat
# COPY filebeat.yml /usr/filebeat/conf.d/filebeat.yml
# COPY filebeat.conf /etc/supervisor/conf.d/filebeat.conf 
ADD jdk-8u211-linux-x64.tar.gz /usr/local/
ENV JAVA_HOME=/usr/local/jdk1.8.0_211 \
 JRE_HOME=/usr/local/jdk1.8.0_211/jre \
 CLASSPATH=.:/usr/local/jdk1.8.0_211/lib:/usr/local/jdk1.8.0_211/lib
ENV PATH $PATH:$JAVA_HOME/bin
