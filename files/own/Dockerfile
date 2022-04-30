FROM node:18-alpine

EXPOSE 80

RUN apk add --update tini

WORKDIR /usr/src/app

COPY package.json package.json

RUN npm install && npm cache clean

COPY . .

CMD ["tini", "--", "node", "./bin/www"]