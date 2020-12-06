FROM node:14

RUN mkdir /client
WORKDIR /api

COPY package*.json ./

RUN yarn install

COPY . .

EXPOSE 8080