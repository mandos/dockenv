FROM node:14.15.0-alpine3.10

RUN npm install -g vim-language-server
RUN apk --no-cache add python3 \
  && pip3 install -U pip \
  && pip3 install --no-cache-dir vim-vint \
  && pip3 uninstall --yes pip \
  && cd /usr/bin && ln -s python3 python
ENTRYPOINT []
