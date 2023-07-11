
FROM ubuntu:18.04

RUN apt-get update; apt-get install -y curl nano sudo gnupg iputils-ping git glibc-source

RUN useradd -m user && echo "user:user" | chpasswd && adduser user sudo

WORKDIR /home/user/

# CMD ["/bin/sh" "-c" "/bin/bash"]

CMD ["/bin/bash"]