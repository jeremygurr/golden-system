FROM util

ARG DOCKER=podman
ARG NO_PROXY=
ARG HTTP_PROXY=
ARG HTTPS_PROXY=

ENV NO_PROXY=$NO_PROXY
ENV HTTP_PROXY=$HTTP_PROXY
ENV HTTPS_PROXY=$HTTPS_PROXY

USER root

COPY npmrc /home/.npmrc
COPY yarnrc /home/.yarnrc
COPY yarnrc.yml /home/.yarnrc.yml

#RUN npm install -g --ignore-scripts @earendil-works/pi-coding-agent
RUN curl -fsSL https://pi.dev/install.sh | sh

RUN curl -fsSL https://herdr.dev/install.sh | sh
RUN mkdir -p /repo
RUN chown -R util /home /work /repo

USER util

#RUN pi update
#RUN pi update --extensions

WORKDIR /work
CMD /bin/bash

