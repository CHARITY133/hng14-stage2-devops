FROM node:18-alpine

RUN adduser -D appuser
WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

USER appuser

CMD ["npm", "start"]
