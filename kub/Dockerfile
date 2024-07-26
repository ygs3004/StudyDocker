FROM node:14-alpine

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 8080

CMD [ "node", "app.js" ]

# 빌드
# docker build -t kub-first-app .

# minikube 상태확인
# minikube status
# 실행중인지 않다면 minikube start --driver=${가상머신}

# deployment 생성, 가상머신이므로 로컬 image가 아닌 hub repository 이용
# kubectl create deployment ${deployment-name} --image=${remote-image}

# deployment 제거
# kubectl delete deployment ${deployment-name}

# deployment 확인
# kubectl get deployments

# pods 확인
# kubectl get pods

# LoadBalancer 이용하여 port 노출 및 service 생성
# kubectl expose deployment ${deployment-name} --type=LoadBalancer  --port=8080

# service 확인
# kubectl get services

# service 접근
# minikube service ${deployment-name}

# 다중 컨테이너 pods 실행
# kubectl scale deployment/${deplyment-name} --replicas=3

# 기존 deployment 컨테이너 새로운 이미지 설정
# kubectl set image deployment/${deployment-name} ${old-image-name}=${new-hub-image:tag}

# deployment update 확인
# kubectl rollout status deployment/${deployment-name}

# deployment history
# kubectl rollout history deployment/${deployment-name}
# kubectl rollout history deployment/${deployment-name} --revision=${revision}

# deployment rollback
# 이전
# kubectl rollout undo deployment/${deployment-name}
# 특정 revision
# kubectl rollout undo deployment/${deployment-name} --to-revision=${revision}

# service 제거
# kubectl delete service ${deployment-name}

# deployment 제거
# kubectl delete deployment ${deployment-name}