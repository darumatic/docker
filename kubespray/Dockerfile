# Pasario Development Container
FROM 687293323933.dkr.ecr.us-east-1.amazonaws.com/centosjava
MAINTAINER Felix Schmitz <Felix.Schmitz@pasar.io>

RUN yum -y install git \
    && mkdir /opt/k8setup \
    && yum -y install epel-release \
    && yum -y install ansible \
    && yum -y install python-pip \
    && pip2 install kubespray \
    && pip install --upgrade pip \
    && pip install Jinja2==2.9.6
WORKDIR /opt/k8setup
