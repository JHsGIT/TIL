Git

`git`은 분산형버전관리시스템(DVCS - Distributed Version Control System)이다.

소스코드의 버전(이력)을 관리할 수 있다.

## 기초 명령어 정리

### 1. git 저장소 설정

```bash
$ git init
```

- 결과 : git bash를 기준으로 **'(master)' **가 표시되는 것을 확인하자
- .git 폴더가 생성된다.

```bash
유지훈@DESKTOP-2KIR9SA MINGW64 ~/Desktop/TIL
$ git init
Initialized empty Git repository in C:/Users/유지훈/Desktop/TIL/.git/

유지훈@DESKTOP-2KIR9SA MINGW64 ~/Desktop/TIL (master)
```

### 2. git add

git add는 현재 working tree 에서 commit할 목록에 담아 놓는 것이다.

그 목록은 보통 staging area라고 부른다.

* 특정 파일 추가

  ```bash
  $ git add a.txt
  ```

* 특정 폴더 추가

  ```bash
  $ git add images/
  ```

* 현재 디렉토리 파일 모두 추가

  ```bash
  $ git add .
  ```

### 3. git commit

git commit은 현재 소스코드의 이력을 남기는 것으로, 현재 커밋할 목록(staging area)에 담겨 있는 파일을 기록한다.

일종의 현재 시점의 스냅샷이 찍히는 것이다.

```bash
$ git status
$ git commit -m '커밋메세지를 입력'
```

* 커밋메세지는 반드시 현재 작업 사항을 알기 쉽게 작성하자!
* 커밋 직전에는 git status를 통해 원하는 파일이 커밋될 수 있는지를 체크한다!

### 4. status/log

CLI(Command line InterFace)에서는 내가 명령어를 치지 않는 이상 현재 상태를 눈으로 확인할 수 없다.

반드시 두가지 명령어를 통해 git의 상태를 확인하자!

```bash
$ git status
$ git log
```

## 원격저장소 활용하기

### 1. push

1. github 저장소(원격저장소)를 origin 이라는 이름으로 설정한다.

   ```bash
   $ git remote add origin https://_________.git
   ```

2.  원격 저장소로 보낸다.

   ```bash
   $ git push origin master
   ```

### 2. pull

1. 원격 저장소로부터 변경사항을 확인하고 가져온다.

   ```bash
   $ git pull origin master
   ```

### 3. Clone

Push/Pull과는 다르게 원격 저장소의 내용을 최초로 받아 올 때 활용한다.

```bash
$ git clone https://______________.git
```

