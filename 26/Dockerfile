FROM fchantada/centos:latest
RUN yum clean all && \
    yum -y install epel-release && \
    yum -y install sshpass PyYAML python-jinja2 python-httplib2 python-keyczar python-paramiko python-setuptools git python-pip
RUN mkdir /etc/ansible/
RUN echo -e '[local]\nlocalhost' > /etc/ansible/hosts
RUN pip install boto3 botocore boto pyopenssl passlib
RUN pip install ansible==2.6.*