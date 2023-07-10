
FROM ubuntu:latest

RUN apt-get update; apt-get install -y curl nano sudo gnupg iputils-ping git

RUN useradd -m user && echo "user:user" | chpasswd && adduser user sudo

WORKDIR /home/user/

CMD ["/bin/sh" "-c" "/bin/bash"]

# CMD ["/bin/bash"]