FROM node:20-alpine AS build

WORKDIR /app

COPY . .

RUN npm install

RUN npm run build

COPY /usr/app/dist/index.html /usr/app/dist/200.html

FROM nginx:1.27-alpine

ARG PORT
EXPOSE $PORT

COPY ./docker/nginx/conf.d/default.conf /etc/nginx/conf.d/default.conf
COPY --from=build /usr/app/dist /usr/share/nginx/html