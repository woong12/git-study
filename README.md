<h1>About Git & GitHub</h1>

# BASIC GIT CONCEPTS

## Requirements

1. git, 편집에디터(ex.VSC), github desktop 설치
2. Window의 경우 cmd 창에서 git --version 입력하여 git 버전 확인
3. GitHub Desktop

## What is Git & GitHub

Git
Git은 Distributed Version Controll System(분산 버전 관리 시스템)으로 파일들을 추적하는 방식이다.

GitHub, GitLab, Bitbucket
Cloud Git Provider들로 우리가 작업한 git 파일(git 변경사항)들을 올리는 일종의 저장소이다.

Github
https://github.com

Gitlab
https://about.gitlab.com

Bitbucket
https://bitbucket.org/product

## Repository

Repository는 사용자의 파일들이 위치한, 깃이 주시하고 있는 폴더이다.
Repository는 .git이라는 폴더를 가지게 되고, 이 폴더에는 깃에 관련된 명령어나 파일, 히스토리들이 있다.
깃은 해당 폴더를 통해 Repository 내부의 변경사항들을 추적할 수 있다.

## Commit

커밋은 기본적으로 작업에 대한 기록이다.
작업중인 폴더에 어떤 변경사항이 있을 때 그것을 히스토리로 기록하고 싶을 때 사용한다.

## Areas

Git workflow(Git Area)는 기본적으로 3단계로 나눠져 있다.

1. Working Directory(Unstage Area)
   우리가 현재 작업하고 있는 폴더로 생성, 수정, 삭제한 파일들이 있는 디렉토리

2. Staging Area
   Index라고도 부르며 , 변경사항이 있는 파일들을 선택해 커밋할 수 있도록 지정하는 곳
   (버전을 만들기 위해 준비 중인 파일들의 스냅샷 데이터가 저장된 곳)

3. Git Directory(Local Repository)
   파일들이 커밋된 곳으로, 파일들의 변경사항에 대한 스냅샷을 가지고 있는 곳
   (Staging Area를 거쳐 만들어진 버전들이 저장된 곳)

Git workflow Lifecycle
https://www.gyanblog.com/git/practical-guide-how-work-git-basic-commands-workflows

## Branches

Branch
브랜치는 main 또는 master 브랜치의 마지막 커밋으로부터 다른 타임라인을 가지게 될 부분이다.
독립적으로 어떤 작업을 진행하기 위한 개념으로, 필요에 의해 만들어지는 각각의 브랜치는 다른 브랜치의 영향을 받지 않기 때문에, 여러 작업을 동시에 진행할 수 있습니다.
https://www.nobledesktop.com/learn/git/git-branches

깃 충돌 (Conflict) 주의사항

- 처음에 chapter_one.txt를 마스터 브랜치에 커밋까지 하고나서, 그 후 happy-ending과 sad-ending 브랜치를 만들어 주셔야 합니다.
- 그 전에 만들게 되면 마스터 브랜치에 있는 chapter_one.txt파일이 없기 때문에 충돌이 날 수 있습니다.
- 마스터 브랜치나 happy-ending, sad-ending 브랜치에서 변경을 하고 나면 반드시 커밋을 해준 후에 Update나 Merge를 해야합니다.

## Conflicts in Branches

expo branch확인
https://github.com/expo/expo/branches

git merge 브랜치명: 다른 브랜치에서 작업한 내용을 현재 브랜치로 병합하기

# GITHUB

## Fork

fork란?
fork는 하나의 저장소에 대한 하나의 복사본입니다.
리포지토리를 fork해서 기존 프로젝트에 영향을 주지 않고 변경 사항을 자유롭게 테스트할 수 있습니다.
https://docs.github.com/en/get-started/quickstart/fork-a-repo

Git Clone CLI
git clone 리포지토리 주소

## Pull Requests

Pull Request란?
원격 저장소의 특정 branch에 push 하고 나면 프로젝트 관리자에게 이 내용을 알리고 내가 수정한 코드를 검토 후 병합해달라고 요청하는 것을 말한다.
코드 충돌을 최소화할 수 있고 push 권한이 없는 프로젝트나 오픈 소스 프로젝트에 기여할 때 많이 사용합니다.

Pull Request 과정

1. Fork
   Upstream Repository(원본 리포지토리)를 자신의 저장소로 fork

2. Clone, Remote설정 (git clone 깃URL)
   fork해온 리포지토리를 로컬 저장소로 Clone

3. Branch 생성 (git checkout -b 브랜치명)
   클론해온 프로젝트의 코드를 추가, 수정할 때 브랜치를 생성해서 작업할 수 있다.

4. 수정 작업 후 add, commit, push
   작업 완료 후 add, commit, push를 통해 해당 코드를 원격 저장소로 푸시

5. Pull Request 생성
   원본 리포지토리에서 New pull request를 통해 Pull Request 생성

6. Merge Pull Request
   해당 리포지토리의 관리자는 코드의 변경 사항을 확인 후, Merge여부를 결정

7. Merge 이후 동기화 및 Fork 및 Branch 삭제
   Merge가 완료되면 로컬에 작성한 코드와 원본의 코드를 병합하고 최신의 상태를 유지하게 위해 동기화

## Origin and Upstream

Upstream Branch
Upstream Branch는 fork해온 베이스 저장소의 마스터 브랜치와 연결되어 있는 브랜치이다.
Upstream Branch를 통해 메인 리포지토리의 최신 커밋 수정 사항들을 현재 작업중인 브랜치로 가져올 수 있다.

오픈 소스 프로젝트에서 협업하는 방법
https://www.tomasbeuzen.com/post/git-fork-branch-pull

## Issues

Issue
프로젝트를 관리하기 위한 시스템 중 하나로 아직 미해결된 부분이나 발견된 문제, 버그등에 관한 것들을 이슈로 생성해 기록하는 것이다.
주로 해당 프로젝트를 오픈 소스의 환경에서 작업할 때, 여러 테스터들이 문제를 찾아서 이슈를 적게 된다.

Milestone
버전을 올릴 때 필요한 것들을 따로 리스트로 모아두는 것으로, 프로젝트에서 해결하거나 달성해야 할 이슈들을 모아서 그 프로젝트의 진척을 보기 위해 사용되는 기능이다.
마일스톤은 프로젝트의 기간에 영향을 주지는 않지만, 꼭 달성해야만 하는 주요한 목표가 성공에 도달하도록 초점을 맞춘다.
예를 들면 새롭게 추가될 특정 기능이나 새로운 버전업 등이 마일스톤이 될 수 있다.

# CLI

## CLI log, commit, push

Git CLI

git log: 커밋 히스토리 확인
git add 파일명: 하나의 변경된 파일을 staging area로 이동
git add .: 현재 폴더에 변경된 모든 파일들을 staging area로 이동
git commit -m "커밋 메세지": 커밋하기
git push origin master또는 main: 원격 저장소로 푸시하기

## Checkout and Hard Reset

터미널상태에서 이전 커밋으로 가고싶으면

1. git log 에서 commit ID 확인
2. git checkout 'commit ID'

되돌아오려면
git checkout master

현재 HEAD 기준으로 commit 을 삭제하려면
git reset --hard HEAD
git reset --hard HEAD^ HEAD기준 1개 이전 commit 삭제
git reset --hard HEAD^^ HEAD기준 2개 이전 commit 삭제

로컬에서 삭제된 commit 들을 push 된 origin 에 반영하려면
git push origin master --force

## Mixed Reset

git reset HEAD^

■ 복합 리셋
▷ 커밋만 삭제하고 파일 변경 사항은 그대로 둔다.
▷ 변경 사항들을 unstage 영역에 둔다.

하드 리셋 - 파일 변경 내역을 유지하지 않는다.
복합 리셋 - 변경한 파일의 내용은 그대로 둔다.

■ 원격저장소 확인
git remote -v
■ origin에서 코드가져오기
git pull origin master

## Soft Reset

git reset HEAD^^ --soft

■ 소포트 리셋
▷ 되돌릴 커밋의 변경사항을 unstage 영역에 추가하지 않고
stage 영역에 추가한다.
▷ unstage 영역에 작업중인 파일이 있을 때 섞이지 않고 싶을 때 사용한다.

대부분의 경우에는 하드 리셋이나 복합 리셋을 사용하면 된다.

## Checkout Branches

전체 브랜치 확인
git branch

새로운 브랜치 생성
git checkout -b new-branch-name
git switch -c new-branch-name

마스터 브랜치로 돌아가기
git checkout master

로컬 저장소에서 브랜치 삭제
git branch -d 브랜치명

## Amending Commits and Ignoring Files

■ 커밋 수정
▷ 커밋 수정(amend)은 가장 마지막 커밋을 수정하는 것
git commit --amend -m "(메시지)"
git commit --amend --no-edit
--no-edit ▷ 커밋 메세지는 수정하지 않는다

■ 커밋할 때 파일들의 상태보기
git status
▷ stage 영역에 있지 않은 파일은 빨간색으로 표시
▷ stage 영역에 있는 파일은 초록색으로 표시

■ .gitignore파일에 git에 추가하고 싶지 않은 파일이나 폴더 입력
폴더를 추가하는 방법 ▷ /(폴더명)

■ stage 영역에서 제거
git rm -r (제거할 것) --cached
-r ▷ 폴더 제거시 사용

## Origins

■ 원격저장소 목록
git remote -v

■ 원격저장소 추가
git remote add (이름) (url)

■ 원격저장소 제거
git remote remove (이름)
※ 더 간단한 명령어
git remote rm (이름)
