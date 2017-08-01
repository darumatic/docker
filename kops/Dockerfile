# Darumatic container for using kubespray
FROM centos:7
MAINTAINER Felix Schmitz <Felix@darumatic.com>

RUN curl -LO https://github.com/kubernetes/kops/releases/download/1.7.0/kops-linux-amd64 \
    && chmod +x kops-linux-amd64 \
    && mv kops-linux-amd64 /usr/local/bin/kops \
    && yum -y install epel-release \
    && yum -y install python-pip \
    && pip install --upgrade pip \
    && pip install awscli \
    && curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.7.0/bin/linux/amd64/kubectl \
    && chmod +x ./kubectl \
    && mv ./kubectl /usr/local/bin/kubectl \
    && yum -y install groff \
    && yum -y install bind-utils

COPY kops_user.sh /root 
WORKDIR /root
