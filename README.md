# About Git & GitHub

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
