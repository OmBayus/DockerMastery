FROM node:18-alpine

EXPOSE 80

RUN apk add --update tini

WORKDIR /usr/src/app

COPY package.json package.json

RUN npm install

COPY . .

CMD ["npm","start"]