FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

CMD [ "node", "server.js" ]
# 백그라운드에서 'feedback-node:volumes' 이미지를 실행하고, 이름을 'feedback-app'으로 하며, 호스트의 3000번 포트를 컨테이너의 80번 포트에 연결하고, 컨테이너가 종료되면 자동으로 삭제하며, 'feedback' 볼륨을 '/app/feedback'에 마운트합니다.
# docker run -d -p 3000:80 --rm --name feedback-app -v feedback:/app/feedback feedback-node:volumes