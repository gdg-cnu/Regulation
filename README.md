# GDGoC CNU 회칙

## 요약

GDG on Campus Chonnam National University(GDGoC CNU)의 회칙입니다.

[여기](https://gdg-cnu.github.io/Regulation/)에서 확인하실 수 있습니다. 원문은 [`index.md`](index.md)입니다.

## 준비물

- GitHub 계정과 이 레포의 쓰기 권한. 운영진은 `gdg-cnu` org의 `managers` 팀으로 받습니다.
- 그 밖에 설치할 것은 없습니다. 수정은 GitHub 웹 편집기로 하고, 사이트는 GitHub Pages가 `main`을 자동으로 빌드합니다. PoolC처럼 Ruby·Jekyll을 설치할 필요가 없습니다.

## 파일 구성

| 파일 | 내용 | 운영진 승인 |
|---|---|---|
| `index.md` | 회칙 본문과 개정 연혁 | 필요 |
| `_config.yml` | 사이트 제목·테마 | 필요 |
| `.github/CODEOWNERS` | 승인이 필요한 파일 지정 | 필요 |
| `.github/pull_request_template.md` | PR 양식 | 필요 |
| `.github/rulesets/main.json` | `main` 보호 규칙 사본 | 필요 |
| `README.md` | 이 문서 | 불필요 |

## 관리

- 이 레포는 오직 Pull Request로만 업데이트가 가능합니다. `main`에 직접 push, force push, 브랜치 삭제는 막혀 있으며 관리자도 예외가 없습니다.
- 회칙(`index.md`)과 사이트·규칙 설정 파일을 바꾸는 PR은 운영진(`@gdg-cnu/managers`)의 Review가 있어야만 머지할 수 있습니다.
- README만 바꾸는 PR은 승인 없이 바로 머지할 수 있습니다.

### 회칙 개정

1. 총회에서 의결합니다(제27조제2항제2호). 개정안은 총회 7일 전까지 공지해야 하고 기간을 줄일 수 없으며(제29조제2항), 재적 활동회원 과반수 출석과 출석 과반수 찬성으로 의결합니다(제31조).
2. GitHub에서 `index.md`를 열고 연필 아이콘(Edit this file)을 눌러 의결된 문구 그대로 고칩니다. 맨 아래 **개정 연혁** 표에 의결일을 한 줄 추가합니다.
3. **Commit changes...** 에서 "Create a new branch for this commit and start a pull request"를 고르고 PR을 만듭니다. 템플릿(개정 내용, 총회 일자, 회의록)을 채우고, PR 제목은 `2026년 2학기 GDGoC CNU 회칙 개정`처럼 씁니다.
4. 운영진 1명이 의결 내용과 같은지 확인하고 승인합니다. 자기 PR은 스스로 승인할 수 없습니다.
5. **Squash and merge** 합니다. PR 제목(과 PR 번호)이 `main`의 커밋 메시지가 되고, 1~2분 뒤 사이트에 반영됩니다. 개정 회칙은 의결일부터 7일이 지난 날 시행됩니다(제55조).
6. 사이트에서 바뀐 부분이 제대로 보이는지 확인합니다. 사이트는 GitHub 미리보기와 다른 변환기(kramdown)를 써서 결과가 다를 수 있습니다. 예를 들어 줄 맨 앞의 `2026. 7. 23.`은 번호 목록으로 바뀌기 때문에 날짜는 표 안에 씁니다.

### 운영진이 바뀔 때

- 회칙 개정 PR은 `managers` 팀에서 작성자가 아닌 사람이 승인해야 머지됩니다. 팀에 현역 운영진이 최소 2명 있어야 합니다.
- 새 회장·운영진이 정해지면 org owner가 org 설정의 **Teams → `managers`** 에서 구성원을 바꿉니다. 졸업한 사람은 뺍니다.
- org owner 권한(공용 계정 `GDG-on-Campus-CNU` 포함)은 회장이 바뀔 때 함께 넘깁니다.

### 설정이 사라졌을 때

org 이전 등으로 레포 설정이 초기화되면 레포 관리자가 다시 맞춥니다.

- **보호 규칙**: 원본은 [`.github/rulesets/main.json`](.github/rulesets/main.json)입니다. 아래 명령으로 다시 적용하고, 켜고 끄는 것은 **Settings → Rules → Rulesets** 에서 합니다.

  ```bash
  gh api -X POST repos/gdg-cnu/Regulation/rulesets --input .github/rulesets/main.json
  ```

- **사이트**: **Settings → Pages** 에서 Source를 "Deploy from a branch", Branch를 `main` / `/ (root)`로 둡니다.
- **커밋 메시지**: **Settings → General → Pull Requests** 에서 "Allow squash merging"의 기본 메시지를 "Pull request title"로 둡니다.
