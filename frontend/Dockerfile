FROM node:14-alpine

RUN apk update && \
    apk add --no-cache git

RUN npm install -g expo-cli

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

EXPOSE 19000
EXPOSE 19001
EXPOSE 19002

CMD ["npm", "start", "--web"]
