FROM node:20-alpine AS build

WORKDIR /app

COPY . .

RUN npm install

RUN npm run build

ARG PORT
EXPOSE $PORT

RUN npm install -g serve

COPY --from=build build/index.html build/200.html

CMD ["serve", "-s", "build", "-p", [$PORT]]