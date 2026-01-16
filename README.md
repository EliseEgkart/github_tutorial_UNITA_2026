# UNITA 2026 협업을 위한 Git/GitHub 교육자료

## 교육 목적
- 팀 프로젝트에서 Git/GitHub 기반 협업 흐름을 이해한다.
- 로컬/원격 저장소 개념을 구분한다.
- 브랜치 기반 작업과 PR 생성 과정을 수행한다.
- 작은 단위 커밋과 PR 리뷰 문화를 체험한다.
- 충돌 해결의 기본 절차를 습득하고 재현한다.
- 팀 코드 컨벤션을 준수한다.

## git, Github에 대하여.
![Git flow](img/git_img.png)
### git이란?
Git은 소스 코드의 변경 이력을 체계적으로 관리하기 위한 분산 버전 관리 시스템(DVCS)이다. 파일이 언제, 왜, 어떻게 변경되었는지를 커밋 단위로 기록하며, 각 개발자가 자신의 로컬 환경에서 독립적으로 브랜치를 생성·수정·실험할 수 있다. 중앙 서버에 의존하지 않고도 모든 이력을 보존할 수 있어, 협업 과정에서 충돌을 최소화하고 안정적으로 개발 흐름을 관리하는 데 핵심적인 역할을 한다.

### Github란?
GitHub는 Git 저장소를 온라인에서 호스팅하고 협업을 지원하는 플랫폼 서비스이다. 원격 저장소를 통해 코드 공유, 이슈 관리, 코드 리뷰(Pull Request), 프로젝트 문서화, CI 연동 등 팀 개발에 필요한 기능을 통합적으로 제공한다. 단순한 코드 보관소를 넘어, 오픈소스 협업과 개발자 포트폴리오, 프로젝트 관리의 중심 허브로 활용된다.

## Git / GitHub 명령어 정리 (UNITA)
| 목적 | 명령어 | 설명 |
|:--|:--|:--|
| <div align="center">--------</div> | <div align="center">**# Git 기본 명령어 (로컬 작업 중심) #**</div> | <div align="center">--------</div> |
| 저장소 초기화 | `git init` | 현재 디렉토리를 Git 저장소로 초기화 |
| 상태 확인 | `git status` | 변경/스테이징/커밋 상태 확인 |
| 변경 파일 비교 | `git diff` | 마지막 커밋 대비 변경 내용 확인 |
| 스테이징 비교 | `git diff --staged` | add된 파일과 커밋 차이 |
| 파일 추가 | `git add <file>` | 특정 파일 스테이징 |
| 전체 추가 | `git add .` | 변경된 모든 파일 스테이징 |
| 커밋 | `git commit -m "메시지"` | 변경 이력 기록 |
| 커밋 수정 | `git commit --amend` | 마지막 커밋 수정 |
| 로그 확인 | `git log` | 전체 커밋 이력 |
| 요약 로그 | `git log --oneline --graph --all` | 브랜치 흐름 확인 |
| 커밋 조회 | `git show <hash>` | 커밋 상세 내용 |
|  |  |  |
| <div align="center">--------</div> | <div align="center">**# 브랜치 관련 명령어 (협업 핵심) #**</div> | <div align="center">--------</div> |
| 브랜치 목록 | `git branch` | 로컬 브랜치 확인 |
| 전체 브랜치 | `git branch -a` | 로컬 + 원격 브랜치 확인 |
| 브랜치 생성 | `git branch <name>` | 브랜치 생성 |
| 브랜치 이동 | `git switch <name>` | 브랜치 전환 (`checkout` 가능) |
| 생성+이동 | `git switch -c <name>` | 브랜치 생성 후 이동 |
| 브랜치 삭제 | `git branch -d <name>` | 병합 완료 브랜치 삭제 |
| 강제 삭제 | `git branch -D <name>` | 병합 여부 무시하고 삭제 |
|  |  |  |
| <div align="center">--------</div> | <div align="center">**# 원격 저장소(GitHub) 연동 #**</div> | <div align="center">--------</div> |
| 원격 확인 | `git remote -v` | 원격 저장소 주소 확인 |
| 원격 추가 | `git remote add origin <url>` | GitHub 저장소 연결 |
| 원격 수정 | `git remote set-url origin <url>` | 원격 주소 변경 |
| 업로드 | `git push origin <branch>` | 원격 저장소에 브랜치 반영 |
| 최초 업로드 | `git push -u origin <branch>` | upstream 설정 |
| 내려받기 | `git pull` | 원격 변경 병합 |
| 변경만 수신 | `git fetch` | 병합 없이 원격 변경 수신 |
|  |  |  |
| <div align="center">--------</div> | <div align="center"> **# 병합(Merge) & 충돌 해결 #**</div> | <div align="center">--------</div> |
| 병합 | `git merge <branch>` | 현재 브랜치로 병합 |
| 병합 취소 | `git merge --abort` | 병합 중단 |
| 충돌 확인 | `git status` | 충돌 파일 확인 |
| 해결 표시 | `git add <file>` | 충돌 해결 완료 표시 |
| 병합 커밋 | `git commit` | 병합 완료 |
|  |  |  |
| <div align="center">--------</div> | <div align="center">**# 되돌리기 / 복구 (실수 대비) #**</div> | <div align="center">--------</div> |
| 파일 복구 | `git restore <file>` | 수정 내용 취소 |
| 스테이징 취소 | `git restore --staged <file>` | add 취소 |
| 커밋 되돌림 | `git revert <hash>` | 이력 유지하며 되돌림 |
| 커밋 취소 | `git reset --soft HEAD~1` | 커밋만 취소 |
| 강제 초기화 | `git reset --hard HEAD~1` | 모든 변경 삭제 ⚠️ |

##  