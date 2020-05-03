# react build > docker nginx webserver

# docker

```js
docker pull nginx
docker run -it -p 3002:80 --name webserver nginx
docker exec -it webserver bash
```

```js
sites-available : 가상 서버 환경들에 대한 설정 파일들이 위치하는 부분입니다. 가상 서버를 사용하거나 사용하지 않던간에 그에 대한 설정 파일들이 위치하는 곳이다.

sites-enabled : sites-available 에 있는 가상 서버 파일들중에서 실행시키고 싶은 파일을 symlink로 연결한 폴더입니다. 실제로 이 폴더에 위치한 가상서버 환경 파일들을 읽어서 서버를 세팅합니다.

nginx.conf : Nginx에 관한 설정파일로 Nginx 설정에 관한 블록들이 작성되어 있으며 이 파일에서 sites-enabled 폴더에 있는 파일들을 가져옵니다.
```
