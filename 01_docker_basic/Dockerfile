# 이 예제 파일은 'Docker 기본 명령어 학습'을 목적으로 제작되었습니다.

# Dockerfile 작성
# Nginx 웹 서버를 이용해 파일을 서빙하기 위해, Nginx를 기반으로 한 이미지를 사용하도록 설정하고, 현재 디렉토리의 파일을 컨테이너의 /usr/share/nginx/html 에 복사하도록 지정합니다.
FROM nginx:latest
COPY . /usr/share/nginx/html

# 이미지 빌드
# 빌드하기 전 Dockerfile이 있는 디렉토리에서 다음 명령어를 실행하여 Docker 이미지를 빌드합니다.
# -t는 이미지 이름을 지정하라는 옵션이고, '.'은 현재 위치한 디렉토리를 뜻합니다.
docker build -t my-web-server .

# 컨테이너 생성 및 실행
# 다음 명령어로 Docker 컨테이너를 생성합니다.
# -d는 컨테이너를 백그라운드 상태로 실행하도록 하는 옵션, -p는 컨테이너의 80번 포트를 호스트의 80번 포트에 매핑하는 옵션입니다. my-web-server는 컨테이너를 생성할 때 사용한 이미지 이름입니다.
docker run -d -p 80:80 my-web-server

# 컨테이너 목록 확인
# 다음 명령어로 현재 실행 중인 Docker 컨테이너 목록을 확인합니다.
docker ps

# 컨테이너 삭제
# 다음 명령어로 컨테이너를 중지하고, 삭제합니다. --force 명령어를 통해 중지하지 않은 채로 즉시 삭제할 수 있습니다.
docker stop 컨테이너_ID
docker rm 컨테이너_ID
docker rm --force 컨테이너_ID