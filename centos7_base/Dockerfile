FROM centos:7
COPY CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo
RUN yum update -y && \
 yum reinstall -y glibc-common && \
 yum install -y iputils nc net-tools kde-l10n-Chinese && \
 yum clean all && \
 rm -rf /tmp/* && rm -rf /var/cache/yum/* && \
 localedef -c -f UTF-8 -i zh_CN zh_CN.UTF-8 && \
 rm -rf /etc/localtime && ln -s /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
ENV LANG=zh_CN.UTF-8 \
 LANGUAGE=zh_CN:zh \
 LC_ALL=zh_CN.UTF-8
