FROM node:18-alpine

WORKDIR /app

COPY ./package* .

RUN npm ci

COPY . .

RUN npm run build:server

EXPOSE 5432

CMD ["node", "./dist/server.js"]