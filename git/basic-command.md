# Git command
> git 기본 명령어

- git: 분산 버전 관리 시스템
    - code 변화를 잘 정리하기 위해 사용
    - 소스 코드나 파일의 변화를 추적하고 여러 사람이 함께 작업할 때 협업을 용이하게 해주는 도구


## init
- 현재 위치에 ` .git` 폴더를 생성
- git init 을 활용한 파일 안밖으로 또 git init 사용하면 오류생길 수 있음

```bash
git init
```


## add
- working directory -> staging aree
- `git add .`: 현재 디렉토리와 하위 디렉토리에 있는 모든 변경 사항을 staging aree 에 추가. `.`은 현재 디렉토리를 나타냄.

```bash
git add .
```


## status
- 현재 git 상태 확인

```bash
git status
```


## commit
- 현재 staging aree에 올라간 내용을 스냅샷 찍기
    - `-m` 옵션을 통해 커밋메세지를 바로 입력가능
- 옵션 없이 git commmit을 사용하면 이름 작성하라 나옴
    - git config --global user.email "이메일"
    - git config --global user.name "이름"
- 또 옵션 없이 git commmit을 사용하면 커밋메세지 적으라고 나옴
    - `-m "name"`:메세지 작성하는 옵션

```bash
git commit -m "first commit"
```

- git commit -m "" 하면 내 컴퓨터 TIL .git 에만 저장.
- github에 올릴꺼임
    - git은 트리구조. 분기점 brancg는 가지. 제일 굵은 가지를 master(.git)
- git remote add origin https://github.com/cksfuf/TIL.git
    - github 주소를 origin 으로 지정
- git push origin master
    - 내 .git 을 origin 주소로


## remote add
- 원격저장소의 주소를 저장하는 명령어

```bash
git remote add {remote_name} {remoto_url}
```


## push
- 원격장소로 브랜치를 업로드 하는 명령어

```bash
git push {remote_name} master
```

## 다시 저장하고 github로 올리는 명령어
> `git add .` -> `git commit -m "이름"` -> `git push {remote_name} master`


### vscode
- 정의: 소스 코드 편집기. 다양한 프로그래밍 언어 지원.
- 코드 실행: 실행시키고자 하는 파일 들어가서 마우스 오른쪽 코드로 열기
- 터미널 열기: ctrl + `(물결)


### linux basic command
- pwd (print working directory): 현재 작업중인 경로를 표시
- clear (ctrl + l): 터미널 창을 지워주는 명령어
- ls: 현재 폴더에 있는 파일/폴더 목록 표시(ls -a: 숨겨진 목록까지 표시)
- mkdir {directory_name}: 폴더 생성
- touch: 파일 생성
- rm {name}: 파일 삭제(rm -r: 폴더 삭제)
- cd(cgange directory)
	- cd .. : 상위 폴더로 이동
	- cd ~ : 홈(데스크탑)으로 이동
	- cd {directory_name}: 해당 폴더로 이동


### git 과정 한글설명

- 관리하고싶은 상위 파일에 git init -> .git 폴더 생성한거임
- 파일 변경 후 저장 -> 내 컴퓨터에만 있는 .git 폴더 저장된거임
- 저장 후 git add . -> .git 폴더의 모든 파일을 스테이지에 올린거임
- git status -> 현재 git 상태 확인
- git add . 후 git commit -m "커밋메세지" -> 스테이지 위에 있는 애들 사진 찍은거임
- git remote add origin https://github.com/cksfuf/TIL.git -> 내 github 계정의 주소를 origin 으로 지정
- git push origin master -> 사진찍은 .git 폴더를 내 github 계정에 올린거임

- 위 과정 후 관리하는 파일을 변경하여 또 github에 올리고 싶다면?
- git add .
- git commit -m "an"
- git push origin master
- 이것만 반복하셈.