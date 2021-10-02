FROM node:slim

ENV USER="node"

# Install package
RUN apt update && \
    apt install -y bash libglib2.0-0 libnss3 libatk1.0-0 libatk-bridge2.0-0 libcups2 \
    libdrm2 libxkbcommon-dev libasound-dev libxcomposite1 libxdamage1 libxrandr2 libgbm1 \
    libpango-1.0-0 libcairo2 libxshmfence1

# basic setting
USER ${USER}
WORKDIR /home/$USER
RUN usermod -s /bin/bash node
ENV PATH $PATH:/home/$USER/node_modules/.bin

# npm setting
# RUN npm install

CMD ["/bin/bash"]
