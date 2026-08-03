# Codyssey E1-1 Mission

# 개발자용 작업실 구축
## Development Workstation


> 개발자는 코드를 작성하기 전에 코드를 실행하고 관리할 수 있는 환경을 먼저 준비해야 합니다.
>
> 이번 미션에서는 터미널, Git, Docker를 직접 설정하며 개발자가 사용하는 기본 작업 환경을 구축합니다.


---

# 프로젝트 소개


## 목표


개발자가 사용하는 기본 작업 환경을 직접 구축하고,

어디서든 동일한 환경을 다시 만들 수 있는
재현 가능한 개발 환경 구축 방법을 학습합니다.


이번 미션에서는 다음 기술을 실습합니다.


| 기술 | 내용 |
|---|---|
| Linux CLI | 터미널 명령어 사용 |
| File System | 파일 및 폴더 관리 |
| Linux Permission | 파일 접근 권한 관리 |
| Git | 버전 관리 |
| GitHub | 원격 저장소 관리 |
| Docker | 컨테이너 기반 환경 구축 |
| Dockerfile | 실행 환경 자동화 |
| Port Mapping | 네트워크 연결 |
| Bind Mount | 파일 공유 |
| Volume | 데이터 저장 관리 |



---

# 개발 환경


| 항목 | 내용 |
|---|---|
| OS | 작성 예정 |
| Shell | 작성 예정 |
| Terminal | 작성 예정 |
| Editor | VSCode |
| Git Version | 작성 예정 |
| Docker Version | 작성 예정 |



## 환경 확인


```bash
git --version

docker --version

docker info
```



# 개발 워크스테이션 구조


```text
Computer

├── VSCode
│
├── Terminal
│
├── Git
│    │
│    └── Version Control
│
└── Docker
     │
     ├── Image
     │
     └── Container
          │
          └── Application
```



개발자의 기본 작업 흐름:


```text
코드 작성

↓

Git으로 변경사항 관리

↓

Docker로 실행 환경 구성

↓

GitHub를 통해 공유 및 협업
```



---

# 진행 체크리스트


| 단계 | 상태 |
|---|---|
| Terminal 기본 명령어 학습 | ⬜ |
| 파일 시스템 이해 | ⬜ |
| Linux 권한 관리 | ⬜ |
| Git 설치 및 설정 | ⬜ |
| GitHub Repository 생성 | ⬜ |
| Docker 설치 확인 | ⬜ |
| hello-world 실행 | ⬜ |
| Ubuntu Container 실행 | ⬜ |
| Docker 운영 명령어 학습 | ⬜ |
| Dockerfile 작성 | ⬜ |
| Web Server Container 실행 | ⬜ |
| Port Mapping | ⬜ |
| Bind Mount | ⬜ |
| Volume 영속성 검증 | ⬜ |



---

# 핵심 개념 정리


<details>
<summary><strong>1. Terminal & CLI</strong></summary>


## CLI(Command Line Interface)


CLI는 마우스 클릭 대신 명령어를 입력하여 컴퓨터를 제어하는 방식입니다.


개발자는 CLI 환경에서 파일 관리, 프로그램 실행, 서버 관리 등 다양한 작업을 수행합니다.


## GUI와 CLI 비교


| 구분 | GUI | CLI |
|---|---|---|
| 입력 방식 | 마우스 클릭 | 명령어 입력 |
| 사용 난이도 | 쉬움 | 학습 필요 |
| 자동화 | 제한적 | 가능 |
| 개발 활용도 | 낮음 | 높음 |



---

## Terminal


Terminal은 사용자가 명령어를 입력할 수 있도록 제공되는 프로그램입니다.


쉽게 말하면:


> 사람이 컴퓨터에게 명령을 전달하는 창구


입니다.



예:


```bash
pwd
```


결과:


```text
현재 위치 출력
```



---

## Shell


Shell은 터미널에서 입력한 명령어를 해석하고 운영체제가 실행할 수 있도록 전달하는 프로그램입니다.


명령 실행 과정:


```text
사용자

↓

Terminal

↓

Shell

↓

Operating System

↓

실행 결과
```



대표적인 Shell:


| Shell | 설명 |
|---|---|
| bash | Linux 기본 Shell |
| zsh | macOS 기본 Shell |
| PowerShell | Windows Shell |



---

## Linux 기본 명령어


| 명령어 | 기능 |
|---|---|
| pwd | 현재 위치 확인 |
| ls | 파일 목록 확인 |
| ls -la | 숨김 파일 확인 |
| cd | 디렉토리 이동 |
| mkdir | 폴더 생성 |
| touch | 파일 생성 |
| cp | 파일 복사 |
| mv | 이동 및 이름 변경 |
| rm | 파일 삭제 |
| cat | 파일 내용 확인 |



예시:


폴더 생성


```bash
mkdir project
```


파일 생성


```bash
touch index.html
```


파일 확인


```bash
ls
```


</details>


---

<details>
<summary><strong>2. Path(경로)</strong></summary>


## Path란?


Path는 파일이나 폴더가 저장된 위치를 의미합니다.


컴퓨터는 모든 파일을 위치 정보로 관리합니다.



예:


```text
/home/user/project/index.html
```



---

## 절대 경로


절대 경로는 파일의 전체 위치를 표시합니다.


예:


```text
/home/user/project/app/index.html
```


비유:


```text
서울특별시 강남구 테헤란로 123번지
```


처음부터 끝까지 정확한 주소를 작성하는 방식입니다.



---

## 상대 경로


상대 경로는 현재 위치를 기준으로 이동하는 방식입니다.


현재 위치:


```text
/home/user/project
```


명령어:


```bash
cd app
```


결과:


```text
/home/user/project/app
```



비유:


```text
현재 방에서 옆방으로 이동
```



---

## 주요 경로 기호


| 기호 | 의미 |
|---|---|
| . | 현재 위치 |
| .. | 상위 폴더 |
| / | 최상위 경로 |
| ~ | 사용자 홈 디렉토리 |



</details>

<details>
<summary><strong>3. Linux 파일 권한</strong></summary>


## Linux 권한이란?


Linux 운영체제에서는 파일과 폴더마다 접근 권한이 존재합니다.


누가 파일을 읽을 수 있는지,

누가 수정할 수 있는지,

누가 실행할 수 있는지를 관리합니다.



---

## 권한 구조


```text
rwx rwx rwx

소유자  그룹  기타 사용자
```



| 권한 | 의미 |
|---|---|
| r | Read (읽기) |
| w | Write (쓰기) |
| x | Execute (실행) |



---

## 권한 확인


파일 권한은 `ls -l` 명령어로 확인할 수 있습니다.


```bash
ls -l
```



결과 예시:


```text
-rwxr-xr-x  user user app.sh
```



해석:


| 대상 | 권한 |
|---|---|
| 소유자 | 읽기 / 쓰기 / 실행 |
| 그룹 | 읽기 / 실행 |
| 기타 사용자 | 읽기 / 실행 |



---

## chmod


`chmod`는 파일 권한을 변경하는 명령어입니다.


기본 형식:


```bash
chmod 권한 파일명
```



예:


```bash
chmod 755 app.sh
```



---

## 755 권한


```text
rwx r-x r-x
```


의미:


| 대상 | 권한 |
|---|---|
| 소유자 | 읽기 / 쓰기 / 실행 |
| 그룹 | 읽기 / 실행 |
| 기타 사용자 | 읽기 / 실행 |


주로 사용:

- 실행 파일
- 폴더
- 스크립트 파일



---

## 644 권한


```text
rw- r-- r--
```


의미:


| 대상 | 권한 |
|---|---|
| 소유자 | 읽기 / 쓰기 |
| 그룹 | 읽기 |
| 기타 사용자 | 읽기 |


주로 사용:

- HTML 파일
- 문서 파일
- 설정 파일



</details>


---

<details>
<summary><strong>4. Git & GitHub</strong></summary>


## Git


Git은 파일 변경 이력을 관리하는 버전 관리 시스템입니다.


개발자가 코드를 수정할 때:

- 어떤 파일이 변경되었는지
- 언제 변경되었는지
- 이전 상태로 돌아갈 수 있는지


를 관리할 수 있습니다.



---

## Git과 GitHub 차이


| 구분 | Git | GitHub |
|---|---|---|
| 역할 | 버전 관리 도구 | 저장소 공유 플랫폼 |
| 위치 | Local PC | Online Server |
| 목적 | 변경 기록 관리 | 협업 및 공유 |



---

## Git 기본 흐름


```text
파일 수정

↓

git add

↓

git commit

↓

변경 기록 저장
```



---

## Git 저장소 생성


```bash
git init
```


현재 폴더를 Git 저장소로 설정합니다.



---

## 변경 파일 확인


```bash
git status
```


현재 변경된 파일 상태를 확인합니다.



---

## 파일 추가


```bash
git add .
```


변경 내용을 Git 관리 대상으로 추가합니다.



---

## Commit


```bash
git commit -m "first commit"
```


현재 상태를 하나의 버전으로 저장합니다.



---

## Git 사용자 설정


이름 설정:


```bash
git config --global user.name "이름"
```



이메일 설정:


```bash
git config --global user.email "이메일"
```



확인:


```bash
git config --list
```



---

## GitHub 연결


Remote Repository 연결:


```bash
git remote add origin 저장소주소
```



Push:


```bash
git push origin main
```



GitHub를 통해 다른 사람과 프로젝트를 공유할 수 있습니다.



</details>


---

<details>
<summary><strong>5. Docker</strong></summary>


## Docker란?


Docker는 프로그램 실행 환경을 컨테이너 단위로 관리하는 기술입니다.


개발 환경 차이로 발생하는 문제를 줄이고,

동일한 실행 환경을 쉽게 만들 수 있도록 도와줍니다.



---

## 기존 실행 방식의 문제


일반적인 프로그램 실행:


```text
내 컴퓨터

↓

프로그램 설치

↓

환경 설정

↓

실행
```



문제:

- 운영체제 차이
- 라이브러리 버전 차이
- 설정 오류



---

## Docker 실행 방식


```text
Docker Image

↓

Container 실행

↓

Application 실행
```



---

# Image


Image는 컨테이너를 생성하기 위한 설계도입니다.


비유:


```text
Image = 붕어빵 틀
```



Image에는:

- 운영체제 환경
- 프로그램
- 라이브러리
- 설정 정보


가 포함됩니다.



---

# Container


Container는 Image를 실행한 실제 환경입니다.


비유:


```text
Container = 만들어진 붕어빵
```



하나의 Image로 여러 개의 Container를 생성할 수 있습니다.



---

## Docker 기본 구조


```text
Dockerfile

↓

Image 생성

↓

Container 실행
```



---

## Docker 설치 확인


```bash
docker --version
```



Docker 상태 확인:


```bash
docker info
```



---

## Hello World 실행


```bash
docker run hello-world
```



Docker가 정상적으로 설치되었다면
테스트 메시지가 출력됩니다.



</details>


---

# Docker 주요 개념


<details>
<summary><strong>Docker Image와 Container</strong></summary>


## Image


Image는 실행 환경의 저장된 형태입니다.


예:


```text
Ubuntu Image

↓

Ubuntu Container
```



---

## Container


Container는 Image를 실행한 독립적인 환경입니다.


특징:

- 독립 실행 가능
- 빠른 생성 가능
- 삭제 및 재생성 가능



</details>


---

<details>
<summary><strong>Dockerfile</strong></summary>


## Dockerfile이란?


Dockerfile은 Docker Image를 자동으로 생성하기 위한 설정 파일입니다.


직접 환경을 설정하는 대신,

명령어를 작성하면 Docker가 자동으로 환경을 구성합니다.



---

예:


```dockerfile
FROM nginx:alpine

COPY app/ /usr/share/nginx/html/
```



설명:


| 명령어 | 의미 |
|---|---|
| FROM | 사용할 기본 Image 지정 |
| COPY | 파일 복사 |



---

## Image 생성


```bash
docker build -t my-web .
```



---

## Container 실행


```bash
docker run -d -p 8080:80 my-web
```



</details>


---

<details>
<summary><strong>Port Mapping</strong></summary>


## Port Mapping이란?


컨테이너 내부의 포트와
내 컴퓨터의 포트를 연결하는 기능입니다.



예:


```bash
-p 8080:80
```



구조:


```text
내 컴퓨터

8080 Port

↓

Container

80 Port
```



사용자가:

```
localhost:8080
```


으로 접속하면

Container 내부의 웹 서비스로 연결됩니다.



</details>

<details>
<summary><strong>Bind Mount</strong></summary>


## Bind Mount란?


Bind Mount는 호스트 컴퓨터의 파일과
컨테이너 내부 파일을 연결하는 기능입니다.


즉,

내 컴퓨터의 파일을 수정하면
컨테이너 내부에서도 변경된 내용을 바로 확인할 수 있습니다.



---

## 구조


```text
Host Computer

app/index.html

        ↕

Container

/usr/share/nginx/html/index.html
```



---

## 사용 예시


```bash
docker run \
-v ./app:/usr/share/nginx/html \
-p 8080:80 nginx
```



설명:


| 옵션 | 의미 |
|---|---|
| -v | Volume 또는 Mount 연결 |
| ./app | 내 컴퓨터 폴더 |
| /usr/share/nginx/html | Container 내부 경로 |
| -p | Port 연결 |



---

## 특징


장점:

- 코드 수정 즉시 반영
- 개발 환경에서 편리함
- 로컬 파일과 Container 연결 가능


사용 사례:

- 웹 개발
- 코드 개발
- 테스트 환경 구성



</details>


---

<details>
<summary><strong>Docker Volume</strong></summary>


## Volume이란?


Volume은 Container가 삭제되어도 데이터를 유지하기 위한 저장 공간입니다.


Container 내부에 저장한 데이터는 Container 삭제 시 함께 사라질 수 있습니다.


Volume을 사용하면 데이터를 안전하게 보관할 수 있습니다.



---

## Container 데이터 문제


일반적인 경우:


```text
Container 생성

↓

데이터 저장

↓

Container 삭제

↓

데이터 삭제
```



---

## Volume 사용


```text
Volume 생성

↓

Container 연결

↓

데이터 저장

↓

Container 삭제

↓

Volume 데이터 유지
```



---

## Volume 생성


```bash
docker volume create mydata
```



---

## Container 연결


```bash
docker run \
-v mydata:/data \
ubuntu
```



---

## Volume 확인


```bash
docker volume ls
```



---

## 특징


- 데이터 영속성 제공
- Container 재생성 가능
- 데이터 백업 가능



</details>


---

# 실습 기록


## 1. Terminal 실습


### 목표

Linux 기본 명령어를 사용하여
파일과 폴더를 관리합니다.



---

## 사용 명령어


```bash
pwd

ls -la

mkdir

touch

cp

mv

rm

cat
```



---

## 실습 과정


폴더 생성:


```bash
mkdir project
```



폴더 이동:


```bash
cd project
```



파일 생성:


```bash
touch index.html
```



파일 확인:


```bash
ls
```



---

## 결과


실행 결과 캡처:


```
스크린샷 첨부
```



</details>


---

<details>
<summary><strong>2. Linux 파일 권한 실습</strong></summary>


## 권한 확인


```bash
ls -l
```



---

## 권한 변경


```bash
chmod 755 파일명

chmod 644 파일명
```



---

## 확인 과정


변경 전:


```
-rw-r--r--
```



변경 후:


```
-rwxr-xr-x
```



---

## 결과


권한 변경 전/후 캡처:


```
스크린샷 첨부
```



</details>


---

<details>
<summary><strong>3. Git 설정 및 GitHub 연결</strong></summary>


## Git 사용자 설정


```bash
git config user.name

git config user.email
```



확인:


```bash
git config --list
```



---

## Repository 생성


Git 초기화:


```bash
git init
```



파일 추가:


```bash
git add .
```



Commit:


```bash
git commit -m "initial commit"
```



---

## GitHub 연결


Remote 등록:


```bash
git remote add origin Repository_URL
```



Push:


```bash
git push origin main
```



---

## 결과


GitHub Repository 업로드 화면:


```
스크린샷 첨부
```



</details>


---

<details>
<summary><strong>4. Docker Container 실행</strong></summary>


## Docker 버전 확인


```bash
docker --version
```



Docker 상태 확인:


```bash
docker info
```



---

# Hello World 실행


```bash
docker run hello-world
```



결과:


```
Hello from Docker!
```



---

# Ubuntu Container 실행


실행:


```bash
docker run -it ubuntu bash
```



Container 내부 명령:


```bash
ls

echo hello

exit
```



---

## Container 확인


실행 중 Container:


```bash
docker ps
```



전체 Container:


```bash
docker ps -a
```



</details>


---

<details>
<summary><strong>5. Docker 운영 명령어</strong></summary>


## Image 확인


```bash
docker images
```



---

## Container 확인


```bash
docker ps

docker ps -a
```



---

## Container 로그 확인


```bash
docker logs 컨테이너명
```



---

## 리소스 확인


```bash
docker stats
```



---

## Container 삭제


```bash
docker rm 컨테이너명
```



---

## Image 삭제


```bash
docker rmi 이미지명
```



</details>


---

# Docker Web Server 제작


<details>
<summary><strong>Nginx 웹 서버 Container 만들기</strong></summary>


## 프로젝트 구조


```text
project

├── Dockerfile

└── app

    └── index.html
```



---

## index.html 작성


```html
<html>

<body>

<h1>
Hello Docker
</h1>

</body>

</html>
```



---

## Dockerfile 작성


```dockerfile
FROM nginx:alpine

COPY app/ /usr/share/nginx/html/
```



---

## Image 생성


```bash
docker build -t my-web .
```



---

## Container 실행


```bash
docker run -d \
-p 8080:80 \
my-web
```



---

## 접속


브라우저:


```
http://localhost:8080
```



---

## 결과


웹 페이지 출력 화면:


```
스크린샷 첨부
```



</details>


---

# Bind Mount 실습


<details>
<summary><strong>파일 변경 실시간 반영 확인</strong></summary>


## 실행


```bash
docker run \
-v ./app:/usr/share/nginx/html \
-p 8080:80 \
nginx
```



---

## 테스트


1. index.html 수정

2. 저장

3. 브라우저 새로고침

4. 변경 내용 확인



---

## 결과


```
파일 수정 내용 즉시 반영 확인
```



</details>


---

# Volume 영속성 검증


<details>
<summary><strong>Container 삭제 후 데이터 유지 확인</strong></summary>


## Volume 생성


```bash
docker volume create mydata
```



---

## Container 연결


```bash
docker run \
-it \
-v mydata:/data \
ubuntu bash
```



---

## 데이터 생성


```bash
echo hello > /data/test.txt
```



---

## Container 종료


```bash
exit
```



---

## 새로운 Container 실행


```bash
docker run \
-it \
-v mydata:/data \
ubuntu bash
```



확인:


```bash
cat /data/test.txt
```



---

## 결과


Container가 삭제되어도
Volume 데이터가 유지되는 것을 확인합니다.



</details>

# Troubleshooting


<details>
<summary><strong>Case 1. Docker 명령어 실행 오류</strong></summary>


## 문제


Docker 명령어 실행 시 오류 발생


예:


```text
Cannot connect to the Docker daemon
```



---

## 원인


Docker Engine이 실행되지 않은 상태일 수 있습니다.



---

## 확인


```bash
docker info
```



---

## 해결 방법


Docker Desktop 실행 후 다시 확인합니다.


확인:


```bash
docker --version

docker info
```



---

## 결과


Docker 정상 실행 확인



</details>


---

<details>
<summary><strong>Case 2. localhost 접속 실패</strong></summary>


## 문제


Docker Container는 실행되었지만
웹 페이지 접속 불가



---

## 원인


Port Mapping 설정 문제 가능


확인:


```bash
docker ps
```



출력 예:


```text
PORTS

0.0.0.0:8080->80/tcp
```



---

## 해결


Container 실행 시 포트 연결 확인


```bash
docker run -p 8080:80 이미지명
```



접속:


```
http://localhost:8080
```



</details>


---

<details>
<summary><strong>Case 3. Container 내부 파일 변경 불가</strong></summary>


## 문제


Container 내부 파일 수정이 반영되지 않음



---

## 원인


Bind Mount 설정 누락



---

## 확인


Container 실행 옵션 확인


```bash
docker inspect 컨테이너명
```



---

## 해결


Bind Mount 연결


```bash
docker run \
-v ./app:/usr/share/nginx/html \
-p 8080:80 nginx
```



</details>


---

<details>
<summary><strong>Case 4. Permission Denied 오류</strong></summary>


## 문제


파일 실행 또는 수정 시 권한 오류 발생



예:


```text
Permission denied
```



---

## 원인


파일 권한 부족



---

## 확인


```bash
ls -l
```



---

## 해결


권한 변경:


```bash
chmod 755 파일명
```



또는:


```bash
chmod 644 파일명
```



</details>



---

# Repository 구조


최종 Repository 구조:


```text
development-workstation


├── README.md
│
├── Dockerfile
│
├── app
│   │
│   └── index.html
│
├── screenshots
│   │
│   ├── terminal.png
│   │
│   ├── permission.png
│   │
│   ├── docker.png
│   │
│   ├── browser.png
│   │
│   ├── volume.png
│   │
│   └── github.png
│
└── .gitignore
```



---

# .gitignore


Git에 업로드하지 않을 파일을 관리합니다.


예:


```text
.env

node_modules/

*.log

.DS_Store
```




---

## 배운 흐름


```text
Terminal

↓

Linux File System

↓

Permission

↓

Git

↓

GitHub

↓

Docker

↓

Container

↓

Deployment Environment
```



---

# 최종 학습 목표 달성


| 항목 | 결과 |
|---|---|
| 터미널 사용 | 완료 |
| Linux 파일 관리 | 완료 |
| 권한 관리 | 완료 |
| Git 버전 관리 | 완료 |
| GitHub 연결 | 완료 |
| Docker 실행 | 완료 |
| Dockerfile 작성 | 완료 |
| Container 운영 | 완료 |
| Storage 관리 | 완료 |



---
