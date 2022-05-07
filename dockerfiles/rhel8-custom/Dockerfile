FROM redhat/ubi8
LABEL maintainer="Cagri Bayram | caggri@outlook.com"
RUN yum install https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm -y
RUN dnf install iproute openssh-clients openssh-server openssh sshpass sudo -y
RUN yum remove epel-release -y
RUN echo 'root:Docker!' | chpasswd
RUN mkdir -p /var/run/sshd
RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key
RUN ssh-keygen -t dsa -f /etc/ssh/ssh_host_dsa_key
RUN sed -i -e 's/#PasswordAuthentication yes/PasswordAuthentication yes/' /etc/ssh/sshd_config
RUN sed -i -e 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
EXPOSE 22
CMD ["/usr/sbin/sshd","-D"]
