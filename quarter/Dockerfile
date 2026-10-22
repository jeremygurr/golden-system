FROM util

USER root
RUN npm install -g --ignore-scripts @earendil-works/pi-coding-agent
RUN curl -fsSL https://herdr.dev/install.sh | sh
COPY init /init
RUN adduser -h /home -s /bin/bash -D util -u 9999
RUN chown -R util /home /work

USER util
WORKDIR /work
CMD [ "/bin/bash", "/init" ]

