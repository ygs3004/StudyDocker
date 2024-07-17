FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

ENV MONGODB_USERNAME=mongoRoot
ENV MONGODB_PASSWORD=mongoPassword

# CMD ["node", "app.js"]

CMD ["npm", "start"]