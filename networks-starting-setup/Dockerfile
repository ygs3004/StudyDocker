FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

CMD ["node", "app.js"]


# Docker Build
# docker build -t favorites-node .   

# Docker Container Run
# docker run -d --name favorites --rm -p 3000:3000 favorites-node

# 네트워크 만들기
# docker network create favorites-net

# 네트워크 지정하여 컨테이너 실행
# docker run -d --name mongodb --network favorites-net mongo 