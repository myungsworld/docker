#docker

설치과정은 생략. 명령어와 기본설명에 중점을 둠  

docker는 두 가지 개념이 있는데 images 와 container 가 있다.
images는 파일이라고 볼수 있고 container는 프로세스라 볼 수 있다.

- **docker version**
버전 확인  

- **docker pull image:latest**
도커는 운영체제를 통채로 가져오는게 아니라 패키지 매니저만 가져오는것  

- **docker images**  
현재 도커에 있는 파일들 확인  

- **docker run -i -t --name 사용할 이름 image /bin/bash**  
i는 interactive : 사용자가 입출력을 할수 있게 함  
t는 sudo tty : 가상터미널을 emulation 해주는 것   
emulation : 컴퓨터 안에 또다른 컴퓨터를 사용하는 것  
/bin/bash : 실행 할 실행파일을 이 파일(bash)로 하겠다  

- **docker ps -a**  
프로세스 전체 확인 

- **docker start [컨테이너 이름] , docker attach [컨테이너 이름] , docker stop[컨테이너 이름]**  
run과 같은 실행 명령어, 컨테이너가 있을때는 이런식으로 실행 해주면 된다.    

- **Ctrl + P + Q**  
실행을 종료 하지 않고 bash를 빠져나오는 명령어  

- **docker exec [컨테이너 이름]**  
도커 컨테이너는 실행 되고있고 저 exec 명령어를 통해 호스트에서 명령어 제어 가능하다.  

- **docker rm [컨테이너 이름] , docker rmi [image]**  
도커 컨테이너를 지우는 명령어, i명령어로 image 자체를 지울수도 있다.  

- **docker rm `docker ps -a -q`**. 
- **docker rmi -f `docker images -q`**. 
- 프로세스 전체삭제와 이미지 전체삭제 명령어  



