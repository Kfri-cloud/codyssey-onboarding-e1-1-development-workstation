codyssey-onboarding-e1-1-development-workstationhttps
### 코디세이 입학연수과정 E1-1미션(개발자용 작업실)


# 개발 환경 구축 체크리스트 (E1-1)

> 개발 환경을 처음부터 직접 구축하고, Git과 Docker를 활용할 수 있는 환경을 만드는 것을 목표로 합니다.

---

# 0단계. 준비

## 목표
개발에 필요한 프로그램을 설치하고 프로젝트를 시작할 준비를 완료한다.

### 해야 할 것

- [ ] GitHub 회원가입
- [ ] VSCode 설치
- [ ] Git 설치
- [ ] Docker Desktop 또는 OrbStack 설치
- [ ] Docker가 정상 실행되는지 확인
- [ ] GitHub Repository 생성
- [ ] VSCode에서 Repository 열기

---

# 1단계. 터미널 익숙해지기

## 목표
리눅스 기본 명령어를 익히고 파일 및 폴더를 다룰 수 있다.

### 해야 할 것

- [ ] `pwd`
- [ ] `ls`
- [ ] `ls -la`
- [ ] `cd`
- [ ] `mkdir`
- [ ] `touch`
- [ ] `cp`
- [ ] `mv`
- [ ] `rm`
- [ ] `cat`

### 증거

- [ ] 명령어 입력 화면
- [ ] 결과 출력 화면
- [ ] README 기록

---

# 2단계. 파일 권한

## 목표
리눅스 파일 권한의 개념을 이해한다.

### 해야 할 것

- [ ] 파일 생성
- [ ] 폴더 생성
- [ ] `ls -l` 확인
- [ ] `chmod` 변경
- [ ] 변경 전후 비교

### 이해하기

- [ ] `r (Read)`
- [ ] `w (Write)`
- [ ] `x (Execute)`
- [ ] `755`
- [ ] `644`

---

# 3단계. Git

## 목표
Git을 사용할 수 있도록 사용자 정보를 설정한다.

### 해야 할 것

- [ ] `git --version`
- [ ] `git config user.name`
- [ ] `git config user.email`
- [ ] `git config --global init.defaultBranch main`
- [ ] `git config --list`

---

# 4단계. Docker 설치 확인

## 목표
Docker가 정상적으로 설치되었는지 확인한다.

### 해야 할 것

- [ ] `docker --version`
- [ ] `docker info`

---

# 5단계. Docker 첫 실행

## 목표
첫 번째 Docker 컨테이너를 실행한다.

### 해야 할 것

- [ ] `hello-world` 실행
- [ ] 성공 로그 저장

---

# 6단계. Ubuntu 컨테이너

## 목표
Ubuntu 컨테이너 내부에서 명령어를 실행한다.

### 해야 할 것

- [ ] Ubuntu 실행
- [ ] bash 접속
- [ ] `ls` 실행
- [ ] `echo` 실행
- [ ] `exit`

### 이해하기

- [ ] `attach`
- [ ] `exec` 차이

---

# 7단계. Docker 명령어

## 목표
Docker 컨테이너 및 이미지를 관리하는 명령어를 익힌다.

### 해야 할 것

- [ ] `docker images`
- [ ] `docker ps`
- [ ] `docker ps -a`
- [ ] `docker logs`
- [ ] `docker stats`

---

# 8단계. Dockerfile 작성

## 목표
Docker 이미지를 직접 생성한다.

### 해야 할 것

- [ ] `app` 폴더 만들기
- [ ] `index.html` 만들기
- [ ] `Dockerfile` 작성
- [ ] `docker build`
- [ ] `docker run`

---

# 9단계. 포트 매핑

## 목표
컨테이너와 컴퓨터를 연결하여 웹페이지를 실행한다.

### 해야 할 것

- [ ] `-p` 옵션 사용
- [ ] `localhost` 접속
- [ ] 브라우저 화면 캡처

### 이해하기

- [ ] 왜 포트를 연결하는가

---

# 10단계. Bind Mount

## 목표
호스트와 컨테이너의 파일을 연결한다.

### 해야 할 것

- [ ] `-v` 옵션 사용
- [ ] HTML 수정
- [ ] 새로고침
- [ ] 변경 확인

### 이해하기

- [ ] 호스트 파일과 컨테이너 연결

---

# 11단계. Docker Volume

## 목표
데이터를 영구적으로 저장하는 방법을 익힌다.

### 해야 할 것

- [ ] Volume 생성
- [ ] 데이터 저장
- [ ] 컨테이너 삭제
- [ ] 새 컨테이너 생성
- [ ] 데이터 그대로 확인

### 이해하기

- [ ] Volume은 왜 사용하는가

---

# 12단계. GitHub

## 목표
Git 저장소를 GitHub와 연결한다.

### 해야 할 것

- [ ] `git init`
- [ ] `git add`
- [ ] `git commit`
- [ ] `git remote add`
- [ ] `git push`

### 증거

- [ ] GitHub Repository
- [ ] VSCode 로그인 화면

---

# 13단계. README 작성

## 목표
실습 내용을 문서화한다.

### 해야 할 것

- [ ] 실행 환경 작성
- [ ] 명령어 기록
- [ ] Docker 설명
- [ ] Git 설명
- [ ] 포트 설명
- [ ] Volume 설명
- [ ] 권한 설명
- [ ] 트러블슈팅 작성

---

# 14단계. 트러블슈팅

## 목표
실습 중 발생한 문제와 해결 과정을 기록한다.

### 최소 2개 이상 작성

예시

- [ ] Docker 실행 안됨
- [ ] localhost 접속 안됨
- [ ] git push 실패
- [ ] 포트 충돌

---

# 진행 현황

| 단계 | 내용 | 완료 |
|------|------|------|
| 0 | 준비 | ⬜ |
| 1 | 터미널 | ⬜ |
| 2 | 파일 권한 | ⬜ |
| 3 | Git 설정 | ⬜ |
| 4 | Docker 설치 확인 | ⬜ |
| 5 | Docker 첫 실행 | ⬜ |
| 6 | Ubuntu 컨테이너 | ⬜ |
| 7 | Docker 명령어 | ⬜ |
| 8 | Dockerfile 작성 | ⬜ |
| 9 | 포트 매핑 | ⬜ |
| 10 | Bind Mount | ⬜ |
| 11 | Docker Volume | ⬜ |
| 12 | GitHub 연동 | ⬜ |
| 13 | README 작성 | ⬜ |
| 14 | 트러블슈팅 | ⬜ |

---

## 최종 목표

- 개발 환경을 스스로 구축할 수 있다.
- 터미널 명령어를 사용할 수 있다.
- Git으로 버전 관리를 할 수 있다.
- Docker 컨테이너를 생성하고 실행할 수 있다.
- Dockerfile을 작성하고 이미지를 빌드할 수 있다.
- 포트 매핑과 Volume의 개념을 이해한다.
- GitHub에 프로젝트를 업로드할 수 있다.
- README와 트러블슈팅 문서를 작성할 수 있다.
