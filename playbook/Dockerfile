FROM node:slim
SHELL ["/bin/bash", "-c"]
RUN apt update && \
    apt install bash

RUN usermod -s /bin/bash node
COPY ./ /workdir/

ENV PATH /workdir/node_modules/.bin:$PATH
WORKDIR /workdir/

RUN npm install

CMD ["/bin/bash"]
