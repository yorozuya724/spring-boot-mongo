FROM node:17-alpine3.12

WORKDIR /usr/src/app

COPY dist dist
COPY package.json .
COPY ecosystem.config.js .

RUN yarn global add pm2
RUN yarn install --production

CMD ["yarn", "saas:serve"]