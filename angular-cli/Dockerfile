FROM node:8.9

RUN yarn global add @angular/cli \
  && ng set --global packageManager=yarn
RUN mkdir -p /var/lib/angular \
  && chown node:node /var/lib/angular

USER node
WORKDIR /var/lib/angular
