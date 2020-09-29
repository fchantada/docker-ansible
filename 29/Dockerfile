FROM fchantada/centos:latest
RUN yum clean all && \
    yum -y install epel-release && \
    yum -y install sshpass PyYAML python3-jinja2 python3-httplib2 python3-keyczar python3-paramiko python3-setuptools git python3-pip
RUN mkdir /etc/ansible/
RUN pip3 install boto3 botocore boto pyopenssl passlib
RUN pip3 install ansible==2.9.*