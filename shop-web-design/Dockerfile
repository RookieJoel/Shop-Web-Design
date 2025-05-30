FROM node:18-alpine

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm ci

COPY . .

RUN chown -R node:node /usr/src/app

USER node

CMD ["npm", "run", "dev"]
