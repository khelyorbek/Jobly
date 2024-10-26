FROM node:20-alpine AS build

WORKDIR /app

COPY . .

RUN npm install

RUN npm run build

ARG PORT
EXPOSE $PORT

RUN npm install -g serve

CMD ["cp", "build/index.html", "build/200.html;", "serve", "-s", "build"]