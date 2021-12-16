### 도커위에 nginx와 react,express가 포함된 nodejs를 컴포즈하여 올리는 파일입니다.
##### package.json이 있는 최상위 디렉토리에서
docker-compose -f docker_dev up
docker-compose -f docker_dep up

### 꼭 확인하고 수정해야 되는 파일
- docker-compose.yml
- nginx_Dockerfile
- node_Dockerfile
    - 서버를 실행시키는 ENTRYPOINT명령어가 있습니다.
- nginx.conf
    - 어플리케이션 별 라우팅을 설정해주어야합니다.
- start-server.sh
    - 서버 시작 명령어를 입력하주어야 합니다.
### 각 도커파일들은 node와 nginx가 최신버전으로 설정 되어있습니다.
### 사용하는 버전에 맞게 바꿔라.