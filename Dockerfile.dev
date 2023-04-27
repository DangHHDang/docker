FROM node:18.12.0-alpine

WORKDIR /app

COPY package.json ./
COPY package-lock.json ./

RUN npm install 

RUN mkdir node_modules/.cache && chmod -R 777 node_modules/.cache

COPY . .

EXPOSE 3000
ENV CHOKIDAR_USEPOLLING=true
CMD ["npm", "start"]