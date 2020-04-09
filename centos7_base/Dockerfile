FROM centos:7.7.1908
MAINTAINER weiyiysw "weiyiysw@163.com"

ENV BASE_DIR="/home/weiyiysw" \
    TIME_ZONE="Asia/Shanghai"

WORKDIR /$BASE_DIR

RUN set -x \
    && yum update -y \
    && yum install -y iputils nc vim libcurl \
    && ln -snf /usr/share/zoneinfo/$TIME_ZONE /etc/localtime && echo '$TIME_ZONE' > /etc/timezone \
    && yum clean all
