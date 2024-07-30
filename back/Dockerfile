FROM node:lts-alpine3.20 as builder

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

FROM node:lts-alpine3.20

WORKDIR /app

COPY --from=builder /app ./

EXPOSE 8000 

CMD [ "npm", "run", "start-auth" ] 
