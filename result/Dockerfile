FROM node:12.22.9-alpine3.15

WORKDIR /result

COPY ["package.json", "package-lock.json*", "./"]

RUN npm install

COPY . /result

CMD [ "node", "server.js" ]
