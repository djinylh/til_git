# Git

## 1. Git 프로그램 설치

- 프로그램 다운로드: https://git-scm.com
- 64-bit Git for Windows Setup 설치

## 2. Git 버전 확인

- 윈도우 키보드 + R 키보드 : `cmd` 입력

```bash
    git --version
```

- 출력창 확인

## 3. VSCode 에 Git 설정하기

### 3.1. 터미널 환경을 git bash 로 설정하기

- 윈도우, 맥, 리눅스 의 명령창을 통일하기 위함.
- 관리도구 선택 > 설정메뉴 선택
- 설정화면 > `default:Windows` 입력
- `Git Bash` 선택
- 설정화면 닫고, VSCode 재실행 추천

### 3.2. VSCode 에서 Git 옵션 설정하기

- 터미널 실행 : `Ctrl + 백틱` 추천
- git 버전 확인

```bash
git --version
```

- 기본 브랜치명을 `main` 으로 설정

```bash
git config --global init.defaultBranch main
```

- 윈도우, 맥, 리눅스 환경에서 Enter 키 처리를 통일함.

```bash
git config --global core.autocrlf true
```

- 깃 Commit 명령을 VSCode 에서 작성하도록 설정

```bash
git config --global core.editor "code --wait"
```

- 깃 사용자 아이디 설정하기

```bash
git config --global user.name "아이디"
```

- 깃 사용자 아이디 확인하기

```bash
git config --global user.name
```

- 깃 사용자 이메일 저장하기

```bash
git config --global user.email "이메일"
```

- 깃 사용자 이메일 확인하기

```bash
git config --global user.email
```

## 4. 깃 작업하기(실습)

### 4.1. 깃 프로젝트 관리 초기화 하기

```bash
git init
```

### 4.2. 깃 현재 상태 파악하기

```bash
git status
```

### 4.3. 깃 현재 수정된 파일, 폴더 등을 저장하기

- 원하는 파일만 저장하기

```bash
git add README.md
```

- 모든 파일 및 폴더 저장하기(추천)

```bash
git add .
```

### 4.4. 수정 내역 메모 남기기

- 한줄 작업 메모

```bash
git commit -m "깃 작업 관련 설명글작성"
```

- 여러 줄 메모 작성하기 (제목, 상세내용)

```bash
git commit
```

<<<<<<< HEAD
<<<<<<< HEAD

### 4.5. 커밋 내용 컨벤션 알아보기

```bash
[커밋타입] : 커밋 메시지(옵션)
```

- 커밋 타입 : 작업의 분류
- 옵션 : 이슈 또는 수정이 된 작업커밋 번호 또는 추가정보
- 커밋 메시지 : 무엇을 했는지 짧은 내용

#### 4.5.1. 커밋타입

- `[feat]` : 새로운 기능 추가
- `[fix]` : 버그 수정
- `[docs]` : 문서 수정(README.md)
- `[style]` : 코드의 스타일 변경(띄워쓰기, 세미콜론 등)
- `[refector]` : 코드 리팩토링(기능 변경, 코드 정리 등)
- `[test]` : 테스트 코드 추가
- `[chore]` : 기타 (빌드 설정, 패키지 업데이트 등)

#### 4.5.2. 옵션

- 만약 `회원가입 로그인 기능 추가` 라면
- 아래는 이슈 #23 번을 해결하고 기능을 추가했다는 것

```
[feat]:회원가입 로그인 기능 추가(#23)
```

#### 4.5.3. 커밋 내용

- Enter 키를 기준으로 제목과 내용을 구분합니다.

```
[docs] : 커밋 제목

커밋 상세 내용작성

```

### 4.6. 커밋 내용 확인하기

- 기존의 commit 된 내용을 확인하기
- 상세보기

```bash
git log
```

- 간략하게 보기

```bash
git log --oneline
```

- 하나의 commit 상세보기

```bash
git show 커밋아이디
```

### 4.6.1. 각 항목 관련 사항 이해하기

- commit : 고유한 커밋 번호(아이디)
- Author : 작성자
- Date : 날짜
- 메시지 : 상세 내용

### 4.7. 브랜치 작업해 보기

- `나뭇가지` 라는 의미로 원 줄기로 부터 파생되는 것을 말함.
- 원 `소스`로 부터 파생한 새롭게 `분기한 소스` 관리를 말함.
- 브랜치를 생성시에는 add 와 commit 이 완료되어야 함.

#### 4.7.1. 브랜치 생성하기

```bash
git add .
git commit -m "[docs]:브랜치 실습 test 생성하기"
git branch test
```

#### 4.7.2. 브랜치 목록보기

```bash
git branch -v
```

#### 4.7.2. 브랜치 이동하기

```bash
git switch test
```

#### 4.7.3. 브랜치 삭제하기

```bash
git branch -D test
git branch -v
```

#### 4.7.4. 브랜치 합치기

- 브랜치를 하나로 합쳐주기
- 주의 사항 : `main 브랜치에서 test 브랜치 합쳐줄 겁니다.`

```bash
git merge 합쳐주고자하는 브랜치명
```

```bash
git daa .
git commit -m "[docs]:브랜치 실습 test 생성하기"
git branch test
```

### 4.8 깃 브랜치 충돌 해결해보기

---

- git branch -v

====>급하게 추가 업무 들어옴

gitt add.
git commit -m "[docs]:업무 저장"
=====> login 업무를 전달합니다.

git branch login
git branch -v

-- 브랜치 목록
main
login
--
git switch login

- 깃 브랜치를 merge 하면 합쳐진다
- `login 브랜치`에서 나는 로그인 기능을 구현하였다 .

git add .
git commit -m "[feat] : 로그인 기능"

머지를 한 이후에 만들어둔 브랜치는 삭제하기

git branch -m "[feat]: 로그인 기능 적용"

---

github 협업에서 상세히 알아보도록 하자.

# GitHub

## 1. GitHub 회원가입 하기

- https://github.com

## 2. Github 프로젝트(repository) 생성하기

- 만약 til_git 프로젝트 생성했다면, 그 github 에도 동일하게 생성하자.
- public 으로 세팅 : 외부로 소스 공개
- description 은 작성해주자 : 프로젝트 설명

## 3. github 인증하기

### 3.1 무조건 github에 로그인 된 상태로 시도하셔야 합니다.

### 3.2 `윈도우 > 자격 증명 관리자 > windows 자격 증명 `에서 github 확인

- 새로 생성하시길 권장합니다.
- pc 정리 또는 자리 이동시 반드시 삭제하셔야 합니다.

## 4. Github 프로젝트 연결하기

### 4.1 원격 저장소 연결하기 주소 지정하기

- `remote` 는 원격(인터넷)을 말합니다.
- `add` 는 추가하라
- `origin` 은 http 주소를 간략하게 별칭을 준 것 ( 단어는 마음대로 가능) 이는 `원격 이름`을 말함.

```bash
git remote add gogogo https://github.com/djinylh/til_git.git
```

### 4.2 원격 저장소 목록 보기

```bash
git push -u origin main
```

윗 명령어를 적은 이후에는

```bash
git push
```

```bach
git branch --unset-upstream
```

push 디폴트값 없애는 명령어

git push만 적어도 윗 명령어를 자동으로 생성되어 실행된다.

### 4.3 원격 저장소에 소스 등록하기

- 습관적으로 하셨으면 좋은 작업 (ctrl + s)

```bash
git add.
git commit -m "[docs]: 최초 등록"
```

- 소스 업로드를 `"push 한다"`라고 합니다.

- `-u` 옵션을 붙이셨다면 이후로는 `git push`만 하면 됨.

### 4.4 원격 저장소 관리하기

-목록보기

```bash
git remote -v
```

- 삭제하기

```bash
git remote remove 원격 이름
```

- 추가하기

```bash
git remote add 원격 이름 https주소
```

- 이름 바꾸기

```bash
git remote rename 옛이름 새이름
```

### 4.5 추천 작업 순서

```bash
git add .
git commit - m " [docs]: 깃 학습"
git push origin main
```

## 5 Github의 소스를 복사해서 작업하는 법

- git hub 주소를 주의하자
- 코드 소스 기준은 `https`로 진행
- 코드 소스 기준이 `ssh`이면 인증을 다시 처리해야함

### 5.1 실습

- 서울로 출장을 갔다 ( pc없이)
- 서울 사무소에 pc를 지급 받았다.
- pc에 환경설정 진행 (vscode, git)
- D:/student/`test`폴더 생성
- github 사이트에 프로젝트를 'clone'한다.
- github 사이트에 repository를 'clone'한다.

### 5.2 clone

```bash
gif clone 깃허브 주소 .
```

### 5.3 clone 이후의 작업

```bash
git status
git branch -v
git branch 새 이름
git switch 새 이름
작업 진행
git add .
git commit -m "[]작업내용"
git push origin  브랜치 이름
```

대구에 내려와서 ...
git branch -v
목록을 먼저 본 후
git fetch --all
다시

// 내 로컬 브랜치 목록
git branch -v
// 내 깃허브 리모트 브랜치 목록
git branch -r
// 로컬 및 깃허브 모든 브랜치 목록
git branch -a

git switch origin/seoul

# git switch --track -c daegu origin/seoul

# GITHub

# 서울에서 작업완료 함.

```bash
git status
```

```bash
git branch -v
```

```bash
git branch 새 이름
```

```bash
git switch 새 이름
```

작업 진행

```bash
git add .
```

```bash
git commit -m "[]작업내용"
```

```bash
git push origin  브랜치 이름
```

### 5.4 git push 이후 작업

-jeju 폴더는 clone을 하여 진행 함. -`til.git` 폴더는 clone을 할 필요가 있을까요?

- `til.git`은 이미 git 세팅이 되어 있기 때문에 clone은 필요 없다.

### 5.5 기존 프로젝트에서 github 브랜치 적용하기

- 기존 프로젝트에서는 clone 하지 않음
- 기존 프로젝트에서는 fetch 사용
- 1. fetch는 깃허브 에서 모든 브랜치를 가져옴

```bash
git fetch --all
```

- 2. 브랜치 목록 전체 보기 (깃허브, 로컬)

```bash
git branch -a
```

- 3. `새롭게 작업한 깃허브 브랜치`를 `로컬 브랜치로 생성` 만들어서 작업`하기

```bach
 git switch --track -c jeju remotes/origin/seoul
```

## 6. 깃허브 브랜치 삭제하기

- 깃 허브 브랜치 모두 내려 받기

```bash
git fetch --all
```

- 로컬 및 깃허브 브랜치 목록 모두 보기

```bash
git branch -a
```

- 깃허브의 브랜치 삭제하기

```bash
git push 저장소이름 --delete 브랜치이름
```

- 예) git push origin --delete remotes/origin/jeju

git push origin --delete origin/jeju

## 7 . 가능하시면 브랜치는 삭제하지 않기를 권장합니다.

## 8 . 가능하시면 commit의 내용은 삭제, 수정하지 않기를 권장합니다.

