FROM util

ARG DOCKER=podman
ARG NO_PROXY=
ARG HTTP_PROXY=
ARG HTTPS_PROXY=

ENV NO_PROXY=$NO_PROXY
ENV HTTP_PROXY=$HTTP_PROXY
ENV HTTPS_PROXY=$HTTPS_PROXY

USER root

RUN npm install -g --ignore-scripts @earendil-works/pi-coding-agent
#RUN curl -fsSL https://pi.dev/install.sh | sh
RUN npm install -g @jmfederico/pi-web --allow-scripts=node-pty
RUN curl -fsSL https://herdr.dev/install.sh | sh

RUN mkdir -p /repo /data
RUN chown -R util /home /work /repo /data

USER util

RUN pi update
RUN pi update --extensions

WORKDIR /work
CMD /bin/bash

