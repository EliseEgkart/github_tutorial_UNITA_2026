# 실습 안내

## 목표
- clone -> branch -> commit -> push -> PR 흐름을 직접 수행한다.
- 리뷰 반영과 충돌 해결 과정을 경험한다.

## 실습 0: 저장소 준비
1. 저장소를 클론한다.
2. 사용자 정보를 설정한다.

```bash
git config user.name "Your Name"
git config user.email "you@example.com"
```

## 실습 1: 개인 브랜치 생성
1. 브랜치를 생성하고 이동한다.

```bash
git switch -c feature/<이름>-practice
```

## 실습 2: 개인 제출 파일 작성
1. `practice_submission/ex)이름_영문.cpp` 파일을 생성한다.
2. `src/practice.cpp`를 참고해 자기소개 1~2줄을 출력하도록 작성한다.
3. 변경 사항을 커밋하고 원격에 푸시한다.

```bash
git add practice_submission/ex)이름_영문.cpp
git commit -m "feat: add practice submission"
git push -u origin feature/<이름>-practice
```

## 실습 3: PR 만들기
- PR 제목: 작업 요약
- PR 본문: 변경 내용 + 확인한 내용
- 리뷰 요청 후 피드백을 반영한다.

## 실습 4: 충돌 해결
1. 두 사람이 같은 파일(`src/practice.cpp`)의 같은 줄을 수정한다.
2. 먼저 머지된 변경을 `git pull`로 가져온다.
3. 충돌을 해결하고 다시 커밋/푸시한다.

## 제출 체크리스트
- 본인 이름의 브랜치로 작업했다.
- `practice_submission/`에 개인 파일을 추가했다.
- PR을 생성하고 리뷰를 반영했다.
- 충돌 해결을 경험했다.

## 자주 생기는 실수
- `main` 브랜치에 직접 커밋함
- `git add`를 하지 않아 커밋이 비어 있음
- PR 본문에 변경 요약/확인 내용이 없음
