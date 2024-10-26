FROM node:20-alpine AS build

WORKDIR /app

COPY . .

RUN npm install

RUN npm run build

RUN npm install -g serve

FROM build

WORKDIR /app/build

COPY index.html 200.html

ARG PORT
EXPOSE $PORT

CMD ["serve", "-s", "build", "-p", "$PORT"]