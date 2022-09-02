FROM ubuntu:jammy AS base
WORKDIR /usr/local/bin
ENV DEBIAN_FRONTEND=noninteractive
RUN apt update && \
    apt upgrade -y && \
    apt install -y software-properties-common curl git build-essential && \
    add-apt-repository --yes --update ppa:ansible/ansible && \
    apt install -y ansible

FROM base AS user
ARG USERNAME=miguel
ARG USER_UID=1000
ARG USER_GID=$USER_UID
ARG TAGS

RUN addgroup --gid $USER_GID $USERNAME \
    && adduser --gecos $USERNAME --uid $USER_UID --gid $USER_GID --disabled-password $USERNAME \
    && apt update \
    && apt install -y sudo \
    && echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME

USER $USERNAME
WORKDIR /home/$USERNAME

FROM user
COPY . .
CMD ["sh", "-c", "ansible-playbook $TAGS local.yml"]
