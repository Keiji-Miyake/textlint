FROM node:14-slim

# メタ情報の付与
LABEL maintainer="k.miyake01+dev@gmail.com"
LABEL version="1.0"
LABEL description="Node.JS"

ENV NPM_CONFIG_LOGLEVEL info
ENV NPM_CONFIG_PREFIX=/home/node/.npm-global
ENV PATH=$PATH:/home/node/.npm-global/bin
ENV TZ=Asia/Tokyo

USER node

WORKDIR /home/node/app

RUN npm install -g textlint \
        textlint-rule-preset-ja-technical-writing \
        textlint-rule-spellcheck-tech-word

EXPOSE 8888