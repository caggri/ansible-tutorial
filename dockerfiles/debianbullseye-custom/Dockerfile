FROM debian:bullseye-slim
LABEL maintainer="Cagri Bayram | caggri@outlook.com"
RUN echo 'root:Docker!' | chpasswd
RUN apt update -y && apt install iproute2 openssh-server ssh-tools sshpass sudo -y
RUN apt autoremove
RUN sed -i -e 's/#PasswordAuthentication yes/PasswordAuthentication yes/' /etc/ssh/sshd_config
RUN sed -i -e 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN mkdir /var/run/sshd
RUN service ssh start
EXPOSE 22
CMD ["/usr/sbin/sshd","-D"]

