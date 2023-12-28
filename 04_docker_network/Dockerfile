# Docker 네트워크는 여러 컨테이너 간 통신을 관리하는 도구입니다.
# 네트워크를 사용하면 각 컨테이너에 IP 주소를 할당할 수 있고, 컨테이너 간 IP 주소로 연결하여 서로 통신할 수 있습니다.
# 이를 활용하여 여러 컨테이너를 통합하여 하나의 서비스로 구성할 수 있습니다.

# 이 예제는 Docker 네트워크를 사용하여 간단한 컨테이너 간 통신을 구성하는 방법을 보여줍니다.

# 이 예제는 다음 구성 요소로 구성된다고 가정합니다.
# Frontend: Nginx로 실행되는 정적 웹 서버
# Backend: Node.js로 작성된 웹 서버

# 다음 명령어를 실행하여 예제를 실행할 수 있습니다.
docker network create my-network
docker run --name frontend --net my-network -p 80:80 -d nginx
docker run --name backend --net my-network -p 8080:8080 -d node server.js

# 컨테이너를 정리하려면 다음 명령어를 실행합니다.
docker rm -f frontend backend
docker network rm my-network