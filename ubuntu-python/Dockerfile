FROM ubuntu:trusty
RUN apt-get update && apt-get install -y \
  sudo
RUN apt-get update && apt-get install -y \
  python \
  python-pip \
  python3 \
  python3-pip \
  python-virtualenv \
  python-dev \
  python3-dev

# add rscohn1 user with password docker
RUN useradd -ms /bin/bash rscohn1 && echo "rscohn1:docker" | chpasswd && adduser rscohn1 sudo

# turn off color
ADD .bash_aliases /home/rscohn1/

USER rscohn1
WORKDIR /home/rscohn1

