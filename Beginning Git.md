git 초기 설정

```bash
$ git config --global user.name "oneash"
$ git config --global user.email "oneash0824@naver.com"
```

### Git 저장소 생성

현재 디렉토리에 생성

`$ git init`

특정 디렉토리에 생성

`$ git init diretory`

→ `.git`이라는 디렉토리 생성됨. (`.`으로 시작하는 파일이나 디렉토리는 숨김처리 되어서 `ls` 로는 안보임. `ls -a`명령어로 확인 가능)

### Git의 3가지 Area

- Working Directory: 내가 작업하고 있는 프로젝트의 디렉토리
- Staging Area: 커밋을 하기 위해 `$ git add` 명령어로 추가한 파일들이 모여있는 공간
- Repository: 커밋들이 모여있는 장소

### File의 라이프 사이클

- Untracked: Working Directory에 있는 파일이지만, Git으로 버전관리를 하지 않는 상태
- Unmodified: 신규로 파일이 추가되었을 때
- Modified: 파일이 추가된 이후 해당 파일이 수정되었을 때
- Staged: Staging Area에 반영된 상태

### Git 파일 생성 (add)

새로운 파일 생성 (Staging Area로 이동)

```bash
$ git add 파일명
$ git add . # 현재 디렉토리 내의 모든 파일
```

`$ git status` 명령어로 Staging Area 파일 상태 확인

### Git 저장소 반영 (commit)

`$ git commit`

.git 저장소 내에 Staging Area의 모든 파일 저장

```bash
# 커밋 시 메세지 남기기
$ git commit -m "메세지"

# commit 수정
$ git commit --amend

# commit 취소
$ git reset
```

`$ git log` 명령어로 commit history 확인

`$ git diff` → commit된 파일 중 변경된 사항 비교

### Git Log 옵션들

```bash
$ git log -p # --patch. commit의 수정 결과를 보여줌
$ git log -n # 상위 n개의 commit만 보여줌
$ git log --stat # 어떤 파일이 commit에서 수정되고 변경되엇는, 팡리 내 라인이 추가되거나 삭제되었느지 확인
$ git log --pretty=oneline # 각 commit을 한 줄로 출력
$ git log --graph # commit간의 연결된 관계를 아스키 그래프로 출력
$ git log -S 텍스트 # 코드에서 추가되거나 제거된 내용 중 특정 텍스트가 포함되어 있는지 검사
```
