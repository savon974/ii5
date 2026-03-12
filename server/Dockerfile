FROM ubuntu:22.04
RUN apt-get update && apt-get install -y openssh-server python3 sudo
RUN mkdir /var/run/sshd
RUN useradd -m ansible && echo 'ansible:ansible' | chpasswd
RUN echo 'ansible ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
