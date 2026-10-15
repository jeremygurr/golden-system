FROM util

USER root
RUN npm install -g --ignore-scripts @earendil-works/pi-coding-agent
RUN curl -fsSL https://herdr.dev/install.sh | sh
COPY init /home/init
RUN mkdir -p /home/.pi
COPY pi-settings.json /home/.pi
RUN chmod a+rx /home/init
RUN chown -R util /home

USER util
WORKDIR /work
CMD [ "/bin/bash", "/home/init" ]

