FROM myjava:2.0.0
MAINTAINER weiyiysw "weiyiysw@163.com"

ADD filebeat-7.4.2-linux-x86_64.tar.gz /usr

RUN yum install -y epel-release \
    && yum install -y python-pip \
    && pip install supervisor \
    && ln -s /usr/filebeat-7.4.2-linux-x86_64 /usr/filebeat \
    && yum clean all

RUN mkdir -p  -p /var/log/supervisor \
    && mkdir -p /etc/supervisor/conf.d

COPY supervisord.conf /etc/supervisor/supervisord.conf

CMD ["/usr/bin/supervisord"]
