# check and use latest python
FROM python:3.13-slim-bookworm

# ----- do not edit below ----- 

ARG USERNAME=deep_learning_with_docker

# install git and set user and group
RUN apt-get update \
    && apt-get install -y git \
    && groupadd -r $USERNAME \
    && useradd -r -m -g $USERNAME $USERNAME \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

USER $USERNAME

WORKDIR /home/$USERNAME