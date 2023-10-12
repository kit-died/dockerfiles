FROM node:20


# RUN curl -sL https://nodejs.org/dist/v18.16.1/node-v18.16.1-linux-x64.tar.xz -o nodesource_setup.sh


# RUN bash nodesource_setup.sh

# RUN apt-get install -y nodejs build-essential



# RUN curl -fsSL https://deb.nodesource.com/setup_18.x | bash - &&\
# apt-get install -y nodejs

# RUN useradd -m user && echo "user:user" | chpasswd && adduser user sudo

# WORKDIR /home/user/

# RUN corepack enable

USER node

RUN mkdir /home/node/.npm-global

ENV PATH=/home/node/.npm-global/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
ENV NPM_CONFIG_PREFIX=/home/node/.npm-global

RUN mkdir -p /home/node/.cache/yarn
RUN mkdir -p /home/node/.yarn

CMD ["/bin/bash"]