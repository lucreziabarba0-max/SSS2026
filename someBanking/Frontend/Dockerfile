
FROM node:24-alpine

WORKDIR /app

RUN apk add --no-cache git

RUN git clone https://github.com/mmenapace/SomeBankingApp.git .

WORKDIR /app/frontend

RUN npm install

EXPOSE 4200

ENTRYPOINT ["npm", "start", "--", "--host", "0.0.0.0"]
