FROM node:20-alpine AS build1

WORKDIR /app

COPY . .

RUN npm install

RUN npm run build

RUN npm install -g serve

FROM build1 as build2

WORKDIR /app/build

COPY --from=build1 index.html 200.html

ARG PORT
EXPOSE $PORT

CMD ["serve", "-s", "build", "-p", "$PORT"]