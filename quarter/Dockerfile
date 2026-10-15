FROM util

USER root
RUN npm install -g --ignore-scripts @earendil-works/pi-coding-agent
RUN curl -fsSL https://herdr.dev/install.sh | sh

USER util
WORKDIR /work
CMD [ "/bin/bash" ]

