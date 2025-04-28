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
git add [원하는 파일]
```
# GITHub