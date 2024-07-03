# 이미지 설정
FROM node

# 명령어가 실행되는 곳
WORKDIR /app

# 상위 레이어에서 변경점이 있을시 하위 레이어도 다시 실행되므로 순서가 성능 향상에 영향을 줌
# pacakge.json 이 변경되지 않았다면 cashe 이용하여 체크할 수 있음
COPY package.json /app

# COPY 후 실행되는 명령어, WORKDIR 기준으로 실행
RUN npm install

# 이미지 생성시 실행, 외부 파일 위치 / 내부 파일 위치, 상대경로 "./" 사용시 WORKDIR 기준
COPY . /app

# 도커 Container -> Local Machine 에게 열어둘 Port 에 대한 문서화 필수 아님
EXPOSE 80

# 명령어로 포트를 노출해야함
# docker run -p ${server-port}:${container-port} 

# 이미지 생성시(x), 이미지 기반으로 컨테이너 시작시 실행(o)
CMD ["node", "server.js"]