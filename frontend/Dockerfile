FROM node:20-alpine AS build

WORKDIR /app

COPY . .

RUN npm install

RUN npm run build

RUN npm install -g serve

COPY --from=builder /app/build/index.html /app/build/200.html

ARG PORT
EXPOSE $PORT

CMD ["serve", "-s", "build", "-p", "$PORT"]