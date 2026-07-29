codyssey-onboarding-e1-1-development-workstationhttps
### 코디세이 입학연수과정 E1-1미션(개발자용 작업실)


<details>
<summary><strong> 개발 환경 구축 체크리스트 </strong></summary>
개발 환경을 직접 구축하고 Git과 Docker를 활용할 수 있는 환경을 만드는 과정을 단계별로 정리한 체크리스트입니다.

<details>
<summary><strong> 진행 현황 </strong></summary>

  ## 진행 현황

| 단계 | 완료 |
|:---|:---:|
| [준비](#0-준비) | ⬜ |
| [터미널](#1-터미널-익숙해지기) | ⬜ |
| [파일 권한](#2-파일-권한) | ⬜ |
| [Git 설정](#3-git-설정) | ⬜ |
| [Docker 설치 확인](#4-docker-설치-확인) | ⬜ |
| [Docker 첫 실행](#5-docker-첫-실행) | ⬜ |
| [Ubuntu 컨테이너](#6-ubuntu-컨테이너) | ⬜ |
| [Docker 명령어](#7-docker-명령어) | ⬜ |
| [Dockerfile 작성](#8-dockerfile-작성) | ⬜ |
| [포트 매핑](#9-포트-매핑) | ⬜ |
| [Bind Mount](#10-bind-mount) | ⬜ |
</details>


## 0. 준비

### 목표

개발에 필요한 프로그램을 설치하고 프로젝트를 시작할 준비를 완료한다.

### 해야 할 것

#### 설치

- [ ] GitHub 회원가입
- [ ] VSCode 설치
- [ ] Git 설치
- [ ] Docker Desktop 또는 OrbStack 설치

#### 확인

- [ ] Docker가 정상 실행되는지 확인
- [ ] GitHub Repository 생성
- [ ] VSCode에서 Repository 열기

---

## 1. 터미널 익숙해지기

### 목표

리눅스 기본 명령어를 익히고 파일과 폴더를 다룰 수 있다.

### 해야 할 것

#### 기본 명령어

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

#### 실행 결과

- [ ] 명령어 입력 화면
- [ ] 결과 출력 화면

#### 문서화

- [ ] README 기록

---

## 2. 파일 권한

### 목표

리눅스 파일 권한의 개념을 이해한다.

### 해야 할 것

#### 권한 실습

- [ ] 파일 생성
- [ ] 폴더 생성
- [ ] `ls -l` 확인
- [ ] `chmod` 변경
- [ ] 변경 전후 비교

### 이해하기

#### 권한 종류

- [ ] `r (Read)`
- [ ] `w (Write)`
- [ ] `x (Execute)`

#### 권한 숫자

- [ ] `755`
- [ ] `644`

---

## 3. Git 설정

### 목표

Git을 사용할 수 있도록 사용자 정보를 설정한다.

### 해야 할 것

#### Git 설정

- [ ] `git --version`
- [ ] `git config user.name`
- [ ] `git config user.email`
- [ ] `git config --global init.defaultBranch main`
- [ ] `git config --list`

---

## 4. Docker 설치 확인

### 목표

Docker가 정상적으로 설치되었는지 확인한다.

### 해야 할 것

#### 설치 확인

- [ ] `docker --version`
- [ ] `docker info`

---

## 5. Docker 첫 실행

### 목표

첫 번째 Docker 컨테이너를 실행한다.

### 해야 할 것

#### 실행

- [ ] `hello-world` 실행
- [ ] 성공 로그 저장

---

## 6. Ubuntu 컨테이너

### 목표

Ubuntu 컨테이너 내부에서 명령어를 실행한다.

### 해야 할 것

#### 컨테이너 실습

- [ ] Ubuntu 실행
- [ ] bash 접속
- [ ] `ls` 실행
- [ ] `echo` 실행
- [ ] `exit`

### 이해하기

#### 개념

- [ ] `attach`
- [ ] `exec` 차이

---

## 7. Docker 명령어

### 목표

Docker에서 자주 사용하는 명령어를 익힌다.

### 해야 할 것

#### 명령어

- [ ] `docker images`
- [ ] `docker ps`
- [ ] `docker ps -a`
- [ ] `docker logs`
- [ ] `docker stats`

---

## 8. Dockerfile 작성

### 목표

Docker 이미지를 직접 생성한다.

### 해야 할 것

#### 프로젝트 생성

- [ ] `app` 폴더 만들기
- [ ] `index.html` 만들기

#### 이미지 생성

- [ ] `Dockerfile` 작성
- [ ] `docker build`
- [ ] `docker run`

---

## 9. 포트 매핑

### 목표

컨테이너와 컴퓨터를 연결하여 웹페이지를 실행한다.

### 해야 할 것

#### 실행

- [ ] `-p` 옵션 사용
- [ ] `localhost` 접속
- [ ] 브라우저 화면 캡처

### 이해하기

#### 개념

- [ ] 왜 포트를 연결하는가

---

## 10. Bind Mount

### 목표

호스트와 컨테이너의 파일을 연결한다.

### 해야 할 것

#### 실습

- [ ] `-v` 옵션 사용
- [ ] HTML 수정
- [ ] 새로고침
- [ ] 변경 확인

### 이해하기

#### 개념

- [ ] 호스트 파일과 컨테이너 연결

---

## 11. Docker Volume

### 목표

데이터를 영구적으로 저장하는 방법을 익힌다.

### 해야 할 것

#### 실습

- [ ] Volume 생성
- [ ] 데이터 저장
- [ ] 컨테이너 삭제
- [ ] 새 컨테이너 생성
- [ ] 데이터 그대로 확인

### 이해하기

#### 개념

- [ ] Volume은 왜 사용하는가

---

## 12. GitHub 연동

### 목표

Git 저장소를 GitHub와 연결한다.

### 해야 할 것

#### Git 작업

- [ ] `git init`
- [ ] `git add`
- [ ] `git commit`
- [ ] `git remote add`
- [ ] `git push`

### 증거

#### 확인

- [ ] GitHub Repository
- [ ] VSCode 로그인 화면

---

## 13. README 작성

### 목표

실습 내용을 문서화한다.

### 해야 할 것

#### 작성 내용

- [ ] 실행 환경 작성
- [ ] 명령어 기록
- [ ] Docker 설명
- [ ] Git 설명
- [ ] 포트 설명
- [ ] Volume 설명
- [ ] 권한 설명
- [ ] 트러블슈팅 작성

---

## 14. 트러블슈팅

### 목표

실습 중 발생할 수 있는 문제와 해결 과정을 기록한다.

### 발생한 문제 체크

#### Case 1. Docker 관련 문제

- [ ] Docker Desktop 실행 안됨
- [ ] Docker 설치 확인 실패
- [ ] Docker daemon 연결 오류
- [ ] 컨테이너 실행 실패
- [ ] 이미지 빌드 실패

---

#### Case 2. 네트워크 관련 문제

- [ ] localhost 접속 안됨
- [ ] 포트 충돌 발생
- [ ] 포트 매핑 오류
- [ ] 컨테이너 내부 서비스 접근 실패

---

#### Case 3. Git 관련 문제

- [ ] git push 실패
- [ ] GitHub Repository 연결 오류
- [ ] commit 누락
- [ ] branch 오류
- [ ] Git 인증 오류

---

#### Case 4. 파일 및 권한 문제

- [ ] 파일 접근 권한 오류
- [ ] chmod 설정 오류
- [ ] 파일 생성 실패
- [ ] 폴더 접근 권한 문제

---

#### Case 5. Docker 데이터 관리 문제

- [ ] Bind Mount 연결 실패
- [ ] Volume 생성 오류
- [ ] 컨테이너 삭제 후 데이터 손실
- [ ] 파일 변경 사항 반영 안됨
