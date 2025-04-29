# GIT
## 1. Git 프로그램 설치
- 프로그램 다운로드 :https://git-scm.com/
- 64-bit Git for Windows Setup 설치

## 2. Git 버전 확인
- 윈도우 키보드 + R 키보드 : `cmd` 입력
``` bash
    git -- version
```
- 출력창 확인

## VScode 에 Git 설정하기 
### 3.1 터미널 환경을 git bash로 설정하기
- 윈도우, 맥, 리눅스 의 명령창을 통일하려고.
-관리도구 선택 > 설정메뉴 선택
- 설정 화면 > `default:windows` 입력
- `Git Bash` 선택 
- 설정화면을 닫은 후 VSCode 재실행 추천

### 3.2 VScode에서 Git 옵션 설정하기
- 터미널 실행 : `ctrl + backtic ` 추천
- git 버전 확인

```bash
git - -version
```
- 기본 브랜치명을 `main` 으로 설정
```bash
git config --global init.defaultBranch main
```
- 윈도우, 맥, 리눅스 환경에서 Enter 키 처리를 통일함.
```
git config -- global core.autocrlf true
```
- git commit 명령을 VScode에서 작성하도록 설정
```bash
git config --global core.editor "code --wait"
```
- git 사용자 아이디 설정하기
```bash
git config --global use.name "id"
```
- git 사용자 아이디 확인하기
```bash
git config --global use.name
```
- git 사용자 이메일 저장하기
```bash
git config --global user.email "이메일"
```
- git 사용자 이메일 확인하기 
```bash
git config --global user.email
```
## 4. git 작업하기
### 4.1 git 프로젝트 관리 초기화 하기 (실습)
```bash
git init 
```
### 4.2 Git 현재 상태 파악하기
```bash
git status
```
### 4.3 git 현재 수정된 파일, 폴더 등 저장하기
- 원하는 파일만 저장하기
```bash
git add 원하는 파일이름
```
-- 모든 파일 저장하기 (추천)
```bash
git add .
```

### 4.4 메모 남기기
- 한 줄 작업 메모
```bash
git commit -m "깃 잡업 관련 설명글작성"
```
- 여러 줄 메모 작성하기 (제목, 상세내용)
```
git commit
```




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

-jeju 폴더는 clone을 하여 진행 함.
-`til.git` 폴더는 clone을 할 필요가 있을까요?
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


# GITHub