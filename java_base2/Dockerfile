FROM centos:7.7.1908
MAINTAINER weiyiysw "weiyiysw@163.com"

ENV BASE_DIR="/home/weiyiysw" \
    TIME_ZONE="Asia/Shanghai" \
    JAVA_HOME="/usr/lib/jvm/java-1.8.0-openjdk" \
    NACOS_USER="nacos" \
    JAVA="/usr/lib/jvm/java-1.8.0-openjdk/bin/java" \
    LANG=zh_CN.UTF-8 \
    LANGUAGE=zh_CN:zh \
    LC_ALL=zh_CN.UTF-8

WORKDIR /$BASE_DIR

RUN set -x \
    && yum update -y \
    && yum reinstall -y glibc-common \
    && yum install -y java-1.8.0-openjdk java-1.8.0-openjdk-devel iputils nc vim libcurl net-tools kde-l10n-Chinese \
    && localedef -c -f UTF-8 -i zh_CN zh_CN.UTF-8 \
    && ln -snf /usr/share/zoneinfo/$TIME_ZONE /etc/localtime && echo '$TIME_ZONE' > /etc/timezone \
    && yum clean all

RUN mkdir -p app/logs
