FROM node:latest

WORKDIR /usr/src/app

USER node

ARG NODE_ENV
ENV NODE_ENV $NODE_ENV

COPY package.json npm-shrinkwrap.json /usr/src/app/
RUN npm install && npm cache clean

COPY . /usr/src/app/

#EXPOSE 3000

CMD [ "npm", "start" ]
