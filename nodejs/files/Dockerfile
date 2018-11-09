FROM node:latest

RUN useradd --user-group --create-home --shell /bin/false nodejs &&\
  npm install --global npm@4.0.0

ENV HOME=/home/nodejs

COPY package.json $HOME/hello/
RUN chown -R nodejs:nodejs $HOME/*

USER nodejs
WORKDIR $HOME/hello
RUN npm install

USER root
COPY index.js $HOME/hello
RUN chown -R nodejs:nodejs $HOME/*
USER nodejs

CMD ["node", "index.js"]
