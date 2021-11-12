FROM node:alpine
USER root

WORKDIR /home/app

COPY package.json  /home/app/

COPY package-lock.json /home/app/

RUN npm install typescript -g
RUN npm install --forzen-lockfile

COPY ./ /home/app

RUN tsc

EXPOSE 8080

CMD [ "node", "./dist/main.js" ]
