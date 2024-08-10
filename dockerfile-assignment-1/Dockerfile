# NOTE: Developer instructions are in the instructions.md file in this directory.

FROM node:6-alpine

EXPOSE 3000

RUN apk add --no-cache tini

WORKDIR /usr/scr/app

COPY package.json package.json

RUN npm install && npm cache clean --force

COPY . .

CMD [ "/sbin/tini", "--", "node", "./bin/www" ]
