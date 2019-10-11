FROM centos:7
ENV LANG en_US.utf8
RUN echo "Asia/Shanghai" > /etc/timezone
COPY Shanghai /etc/localtime
COPY CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo
RUN yum clean all && yum makecache && yum install -y iputils nc net-tools
