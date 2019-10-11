FROM store/oracle/serverjre:8
ENV LANG en_US.utf8
RUN echo "Asia/Shanghai" > /etc/timezone
COPY Shanghai /etc/localtime
RUN yum install -y iputils nc net-tools
