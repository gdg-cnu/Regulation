# Regulation

GDG on Campus Chonnam National University(GDGoC CNU)의 회칙입니다.

**https://gdg-cnu.github.io/Regulation/** 에서 볼 수 있습니다. 원문은 [`index.md`](index.md)입니다.

## 개정 절차

1. 총회에서 의결합니다(제27조제2항제2호). 개정안은 총회 7일 전까지 공지해야 하고 기간을 줄일 수 없으며(제29조제2항), 재적 활동회원 과반수 출석과 출석 과반수 찬성으로 의결합니다(제31조).
2. 의결된 문구 그대로 `index.md`를 고쳐 PR을 올립니다. 맨 아래 **개정 연혁**에 의결일을 한 줄 추가합니다. 개정 회칙은 의결일부터 7일이 지난 날 시행됩니다(제55조).
3. 운영진(`@gdg-cnu/managers`) 1명이 의결 내용과 같은지 확인하고 승인합니다. 자기 PR은 스스로 승인할 수 없습니다.
4. Squash merge 하면 1~2분 뒤 사이트에 반영됩니다. 개정 1건이 `main` 커밋 1개로 남습니다.

## 보호 규칙

`main`은 PR과 운영진 승인으로만 바뀝니다. 직접 push, force push, 브랜치 삭제는 막혀 있고 관리자도 예외가 없습니다.
규칙 원본은 [`.github/rulesets/main.json`](.github/rulesets/main.json)이며, 설정이 사라지면 다시 적용하면 됩니다.

```bash
gh api -X POST repos/gdg-cnu/Regulation/rulesets --input .github/rulesets/main.json
```
