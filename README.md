codyssey-onboarding-e1-1-development-workstationhttps
### 코디세이 입학연수과정 E1-1미션(개발자용 작업실)

<details>
<summary><strong> 개발 환경 구축 용어 정리 </strong></summary>

# 개발 환경 구축 용어 정리

## 1. 개발 워크스테이션 (Development Workstation)

### 의미

개발자가 프로그램을 만들기 위해 사용하는 개인 개발 환경입니다.

쉽게 말하면:

> 개발자가 코딩하고 테스트하는 나만의 작업실

입니다.

### 구성 요소

- 운영체제(OS)
- 터미널
- Git
- Docker
- 개발 도구(VSCode 등)

예시:

```text
내 컴퓨터
 ├── VSCode (코드 작성)
 ├── Terminal (명령 실행)
 ├── Git (버전 관리)
 └── Docker (실행 환경 관리)
```

---

# 2. CLI (Command Line Interface)

## 의미

마우스로 클릭하는 방식이 아니라 명령어를 입력하여 컴퓨터를 조작하는 방식입니다.

예시:

GUI 방식

```text
폴더 클릭 → 파일 생성
```

CLI 방식

```bash
mkdir project
```

결과:

```text
project 폴더 생성
```

---

# 3. Terminal (터미널)

## 의미

컴퓨터에게 명령어를 입력하는 프로그램입니다.

쉽게 말하면:

> 컴퓨터와 대화하는 창구

입니다.

예시:

```bash
pwd
```

결과:

```text
/home/user/project
```

현재 위치를 확인합니다.

---

# 4. Shell (쉘)

## 의미

터미널에서 입력한 명령어를 해석하여 운영체제에 전달하는 프로그램입니다.

쉽게 말하면:

> 사람이 입력한 명령을 컴퓨터가 이해하는 언어로 바꾸는 통역사

입니다.

대표적인 Shell:

| 종류 | 설명 |
|---|---|
| bash | Linux 기본 Shell |
| zsh | macOS 기본 Shell |
| PowerShell | Windows 기본 Shell |

---

# 5. Linux CLI

## 의미

Linux 운영체제에서 사용하는 명령어 기반 환경입니다.

주요 명령어:

| 명령어 | 기능 |
|---|---|
| pwd | 현재 위치 확인 |
| ls | 파일 목록 확인 |
| cd | 폴더 이동 |
| mkdir | 폴더 생성 |
| touch | 파일 생성 |
| rm | 삭제 |

---

# 6. 절대 경로 (Absolute Path)

## 의미

파일이나 폴더의 전체 위치를 표시하는 방식입니다.

예시:

```text
/home/user/project/app/index.html
```

처음부터 모든 경로를 표시합니다.

비유:

> 서울특별시 강남구 테헤란로 123번지

---

# 7. 상대 경로 (Relative Path)

## 의미

현재 위치를 기준으로 이동하는 경로입니다.

현재 위치:

```text
/home/user/project
```

명령:

```bash
cd app
```

결과:

```text
/home/user/project/app
```

비유:

> 현재 위치에서 옆방으로 이동

---

# 8. 파일 권한 (Permission)

## 의미

파일이나 폴더를 누가 어떻게 사용할 수 있는지 정하는 규칙입니다.

Linux에서는 다음 세 가지로 표현합니다.

```text
rwx
```

---

# 9. r / w / x 권한

## r (Read)

읽기 권한

가능한 작업:

- 파일 내용 확인

---

## w (Write)

쓰기 권한

가능한 작업:

- 파일 수정
- 데이터 변경

---

## x (Execute)

실행 권한

가능한 작업:

- 프로그램 실행

---

# 10. 755 / 644 권한

Linux에서는 권한을 숫자로 표현할 수 있습니다.

구조:

```text
소유자 / 그룹 / 기타 사용자
```

---

## 755 권한

```text
rwx r-x r-x
```

의미:

| 대상 | 권한 |
|---|---|
| 소유자 | 읽기 + 쓰기 + 실행 |
| 그룹 | 읽기 + 실행 |
| 기타 사용자 | 읽기 + 실행 |

주로:

- 폴더
- 실행 파일

에 사용합니다.

---

## 644 권한

```text
rw- r-- r--
```

의미:

| 대상 | 권한 |
|---|---|
| 소유자 | 읽기 + 쓰기 |
| 그룹 | 읽기 |
| 기타 사용자 | 읽기 |

주로:

- 문서
- HTML 파일

에 사용합니다.

---

# 11. Git

## 의미

파일 변경 기록을 관리하는 버전 관리 시스템입니다.

쉽게 말하면:

> 작업 내용을 저장하는 기록 시스템

입니다.

예:

```text
버전 1
 ↓
버전 2
 ↓
버전 3
```

문제가 발생하면 이전 상태로 돌아갈 수 있습니다.

---

# 12. GitHub

## 의미

Git 저장소를 온라인에서 관리하고 협업하기 위한 서비스입니다.

차이:

| Git | GitHub |
|---|---|
| 버전 관리 도구 | 온라인 협업 플랫폼 |
| 내 컴퓨터에서 사용 | 인터넷 저장소 |

비유:

Git:

> 내 컴퓨터 속 작업 기록

GitHub:

> 온라인 공유 저장소

---

# 13. Repository (저장소)

## 의미

프로젝트 파일과 변경 기록이 저장되는 공간입니다.

종류:

## Local Repository

내 컴퓨터에 있는 저장소

## Remote Repository

GitHub 같은 원격 저장소

---

# 14. Docker

## 의미

프로그램 실행 환경을 컨테이너로 만들어 관리하는 도구입니다.

쉽게 말하면:

> 어떤 컴퓨터에서도 같은 환경을 실행할 수 있도록 만드는 기술

입니다.

---

# 15. Container (컨테이너)

## 의미

프로그램과 실행에 필요한 환경을 하나로 묶은 독립 공간입니다.

포함 요소:

```text
프로그램
+
라이브러리
+
설정 파일
```

비유:

> 프로그램 전용 작은 방

---

# 16. Image (이미지)

## 의미

컨테이너를 생성하기 위한 설계도입니다.

비유:

```text
이미지 = 붕어빵 틀
컨테이너 = 만들어진 붕어빵
```

흐름:

```text
Image
 ↓
Container 실행
```

---

# 17. Dockerfile

## 의미

Docker 이미지를 만들기 위한 설정 파일입니다.

예:

```dockerfile
FROM nginx

COPY index.html /usr/share/nginx/html
```

의미:

1. nginx 이미지 사용
2. 웹 파일 복사

---

# 18. Docker Build

## 의미

Dockerfile을 이용하여 이미지를 만드는 과정입니다.

명령어:

```bash
docker build -t my-web .
```

흐름:

```text
Dockerfile
 ↓
Image 생성
```

---

# 19. Docker Run

## 의미

이미지를 기반으로 컨테이너를 실행하는 명령어입니다.

```bash
docker run my-web
```

흐름:

```text
Image
 ↓
Container 실행
```

---

# 20. Docker Daemon

## 의미

Docker 작업을 실제로 처리하는 백그라운드 프로그램입니다.

흐름:

```text
Docker 명령어
      ↓
Docker CLI
      ↓
Docker Daemon
      ↓
Container 생성
```

---

# 21. Port (포트)

## 의미

컴퓨터에서 프로그램을 구분하는 번호입니다.

비유:

> 아파트의 방 번호

예:

```text
localhost:8080
```

의미:

```text
내 컴퓨터의 8080번 포트
```

---

# 22. Port Mapping

## 의미

컴퓨터의 포트와 컨테이너의 포트를 연결하는 기능입니다.

예:

```bash
-p 8080:80
```

의미:

```text
내 컴퓨터 8080번
        ↓
컨테이너 80번
```

---

# 23. Bind Mount

## 의미

호스트 컴퓨터의 파일을 컨테이너와 직접 연결하는 방식입니다.

구조:

```text
내 컴퓨터 파일
      ↕
컨테이너 파일
```

특징:

- 파일 변경 즉시 반영 가능

---

# 24. Volume

## 의미

Docker가 관리하는 데이터 저장 공간입니다.

목적:

> 컨테이너가 삭제되어도 데이터를 유지하기 위해 사용

예:

```text
컨테이너 삭제

데이터 ❌ 삭제

Volume 사용

데이터 ⭕ 유지
```

---

# 25. Log (로그)

## 의미

프로그램 실행 기록입니다.

확인 명령어:

```bash
docker logs 컨테이너명
```

확인 내용:

- 실행 상태
- 오류 내용
- 동작 기록

---

# 26. Debugging (디버깅)

## 의미

문제를 찾고 해결하는 과정입니다.

과정:

```text
문제 발생
 ↓
원인 추측
 ↓
확인
 ↓
수정
 ↓
재실행
```

---

# 27. CI/CD

## 의미

코드 테스트와 배포 과정을 자동화하는 시스템입니다.

## CI (Continuous Integration)

코드 변경을 자동으로 검사하고 테스트

## CD (Continuous Deployment)

검증된 코드를 자동 배포

---

# 28. Docker Compose

## 의미

여러 컨테이너를 한 번에 관리하는 도구입니다.

예:

```text
웹 서버 Container
+
DB Container
```

여러 서비스를 함께 실행할 수 있습니다.

---

# 29. Environment Variable (환경 변수)

## 의미

프로그램 설정 값을 코드 외부에서 관리하는 값입니다.

예:

```text
PORT=8080
MODE=production
```

장점:

- 코드 수정 없이 설정 변경 가능

---

# 30. SSH

## 의미

보안 키를 이용하여 원격 서버나 GitHub에 연결하는 방식입니다.

비교:

| 방식 | 특징 |
|---|---|
| HTTPS | 아이디/비밀번호 기반 |
| SSH | 키 인증 기반 |

---

# 전체 개발 환경 흐름

```text
Terminal
   ↓
Linux 명령어 사용
   ↓
파일 및 권한 관리
   ↓
Git 버전 관리
   ↓
Docker Image 생성
   ↓
Container 실행
   ↓
Port 연결
   ↓
Volume 데이터 저장
   ↓
GitHub 공유
```

</details>
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

- [x] GitHub 회원가입
- [ ] VSCode 설치
- [ ] Git 설치
- [ ] Docker Desktop 또는 OrbStack 설치

#### 확인

- [ ] Docker가 정상 실행되는지 확인
- [x] GitHub Repository 생성
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
