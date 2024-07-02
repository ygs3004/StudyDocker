# 이미지 설정
FROM node

# 명령어가 실행되는 곳
WORKDIR /app

# 이미지 생성시 실행, 외부 파일 위치 / 내부 파일 위치, 상대경로 "./" 사용시 WORKDIR 기준
COPY . /app

# COPY 후 실행되는 명령어, WORKDIR 기준으로 실행
RUN npm install

# 도커 Container -> Local Machine 에게 열어둘 Port
EXPOSE 80

# 이미지 생성시(x), 이미지 기반으로 컨테이너 시작시 실행(o)
CMD ["node", "server.js"]