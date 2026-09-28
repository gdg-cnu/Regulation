# GDGoC CNU 회칙

## 요약

GDG on Campus Chonnam National University(GDGoC CNU)의 회칙입니다.

[여기](https://gdg-cnu.github.io/Regulation/)에서 확인하실 수 있습니다. 원문은 [`index.md`](index.md)입니다.

## 관리

- 이 레포는 오직 Pull Request로만 업데이트가 가능합니다. `main`에 직접 push, force push, 브랜치 삭제는 막혀 있으며 관리자도 예외가 없습니다.
- 회칙(`index.md`)과 사이트·규칙 설정 파일을 바꾸는 PR은 운영진(`@gdg-cnu/managers`)의 Review가 있어야만 머지할 수 있습니다.
- README만 바꾸는 PR은 승인 없이 바로 머지할 수 있습니다.

### 회칙 개정

1. 총회에서 의결합니다(제27조제2항제2호). 개정안은 총회 7일 전까지 공지해야 하고 기간을 줄일 수 없으며(제29조제2항), 재적 활동회원 과반수 출석과 출석 과반수 찬성으로 의결합니다(제31조).
2. 새 브랜치에서 의결된 문구 그대로 `index.md`를 고치고, 맨 아래 **개정 연혁** 표에 의결일을 한 줄 추가합니다.
3. PR을 올리고 템플릿(개정 내용, 총회 일자, 회의록)을 채웁니다. PR 제목은 `2026년 2학기 GDGoC CNU 회칙 개정`처럼 씁니다.
4. 운영진 1명이 의결 내용과 같은지 확인하고 승인합니다. 자기 PR은 스스로 승인할 수 없습니다.
5. Squash merge 합니다. PR 제목이 그대로 `main`의 커밋 메시지가 되고, 1~2분 뒤 사이트에 반영됩니다. 개정 회칙은 의결일부터 7일이 지난 날 시행됩니다(제55조).

### 보호 규칙 복구

규칙 원본은 [`.github/rulesets/main.json`](.github/rulesets/main.json)입니다. org 이전 등으로 설정이 사라지면 다시 적용합니다.

```bash
gh api -X POST repos/gdg-cnu/Regulation/rulesets --input .github/rulesets/main.json
```
