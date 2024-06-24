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


