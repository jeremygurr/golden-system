FROM util

USER root
RUN npm install -g --ignore-scripts @earendil-works/pi-coding-agent
RUN pi update
RUN pi update --extensions
RUN curl -fsSL https://herdr.dev/install.sh | sh
RUN mkdir -p /repo
RUN chown -R util /home /work /repo

USER util
WORKDIR /work
CMD /bin/bash

