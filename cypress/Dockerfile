FROM cypress/browsers:latest

RUN apt-get update; apt-get install -y curl nano sudo gnupg iputils-ping git glibc-source

# RUN useradd -m user && echo "user:user" | chpasswd && adduser user sudo
RUN usermod -l user node
RUN usermod -d /home/user -m user

WORKDIR /home/user/

USER user

RUN mkdir /home/user/.npm-global

ENV PATH=/home/user/.npm-global/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
ENV NPM_CONFIG_PREFIX=/home/user/.npm-global

RUN mkdir -p /home/user/.cache/yarn
RUN mkdir -p /home/user/.cache/Cypress
RUN mkdir -p /home/user/.yarn

CMD ["/bin/bash"]