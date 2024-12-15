FROM node:12

WORKDIR /APP

COPY package.json /APP

RUN npm install

COPY . /APP

EXPOSE 80

CMD ["node", "server.js"]
