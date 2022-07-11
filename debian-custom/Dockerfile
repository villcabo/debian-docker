FROM debian:11

LABEL maintainer="Bismarck Villca bismarck.villca@gmail.com"

RUN apt update && apt install openssh-server sudo -y

# Create debian user
ARG USER=debian
ARG PASS=debian
ENV HOME=/home/$USER

RUN useradd -rm -d $HOME -s /bin/bash -g root -G sudo -u 1000 $USER
RUN echo $USER:$PASS | chpasswd

RUN service ssh start
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]