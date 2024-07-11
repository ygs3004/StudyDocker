FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

ENV PORT 80

EXPOSE $PORT

# VOLUME [ "/app/feedback" ]

CMD ["node", "server.js"]


# docker run -p 3100:80 -d --rm --name app -v ${server.js까지의 폴더 경로, server.js 제외}:/app -v /app/node_modules  feedback-node:volumes
# 더 깊은 경로의 볼륨을 우선시 해서 마운트 되기 때문에 node_modules 는 COPY 시 덮어쓰여지지 않고 npm install 된 상태로 유지, 그 외의 경우 마운트되어 실시간 반영됨


# docker run -d --rm -p 3000:8000 --env PORT=8000  --name feedback-app -v feedback:/app/feedback -v "D:\DEV_PERSONAL\StudyDocker\data-volumes-01-starting-setup:/app:ro" -v /app/node_modules -v /app/temp feedback-node:env
# env 환경변수 예시
# 파일의 경우 --env-file ./.env