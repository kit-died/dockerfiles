FROM athoof/ubuntu:20


# RUN curl -sL https://nodejs.org/dist/v18.16.1/node-v18.16.1-linux-x64.tar.xz -o nodesource_setup.sh


# RUN bash nodesource_setup.sh

# RUN apt-get install -y nodejs build-essential

USER user

# Installing Node
SHELL ["/bin/bash", "--login", "-i", "-c"]
RUN curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash
RUN source /home/user/.bashrc && nvm install --lts
# SHELL ["/bin/bash", "--login", "-c"]

RUN corepack enable
RUN yarn set version stable


RUN mkdir /home/user/.npm-global

ENV PATH=/home/user/.npm-global/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# ENV NPM_CONFIG_PREFIX=/home/user/.npm-global

RUN mkdir -p /home/user/.cache/yarn
RUN mkdir -p /home/user/.yarn

CMD ["/bin/bash"]