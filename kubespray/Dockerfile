# Darumatic container for using kubespray
FROM centos:7
MAINTAINER Felix Schmitz <Felix@darumatic.com>

RUN yum -y install git \
    && mkdir /opt/k8setup \
    && yum -y install epel-release \
    && yum -y install ansible \
    && yum -y install python-pip \
    && pip2 install kubespray \
    && pip install --upgrade pip \
    && pip install Jinja2==2.9.6
WORKDIR /opt/k8setup
