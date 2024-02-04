FROM phusion/baseimage:focal-1.0.0
LABEL maintainer="Gaussai Developers <dev@gaussai.org>"
LABEL description="Dockerised Gaussai, built from Travis"

ARG USER_ID
ARG GROUP_ID

ENV HOME /home/gaussai

# add user with specified (or default) user/group ids
ENV USER_ID ${USER_ID:-1000}
ENV GROUP_ID ${GROUP_ID:-1000}
RUN groupadd -g ${GROUP_ID} gaussai && \
    useradd -u ${USER_ID} -g gaussai -s /bin/bash -m -d /home/gaussai gaussai && \
    mkdir /home/gaussai/.gaussai && \
    chown ${USER_ID}:${GROUP_ID} -R /home/gaussai

COPY bin/* /usr/local/bin/

RUN chmod a+x /usr/local/bin/*

USER gaussai

VOLUME ["/home/gaussai"]

EXPOSE 15905 9999 25905 25906

WORKDIR /home/gaussai
