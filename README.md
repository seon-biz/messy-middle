# 메시미들 비즈니스 진단 스킬

Google × The Behavioural Architects의 「Decoding Decisions」(메시미들) 프레임워크로 **내 비즈니스를 직접 진단**하고, 개선 기획서와 전략 덱까지 만드는 Claude Code 스킬입니다.

상품 하나든, 상품군 전체든, 사업 전체든 — 상세페이지 주소나 소개 자료만 던지면 스킬이 먼저 읽고 필요한 것만 물어봅니다.

## 설치

Claude Code를 열고 이렇게 말하면 끝입니다. (설치 명령 실행 여부를 물으면 허용을 눌러주세요.)

```
https://github.com/seon-biz/messy-middle 이 스킬 설치해줘
```

터미널에서 직접 설치하려면:

```bash
npx skills add seon-biz/messy-middle
```

Claude Code 공식 플러그인 방식(버전 관리, `/plugin` UI에서 켜고 끄기)을 원하면 Claude Code 입력창에 아래 두 줄을 순서대로 입력합니다.

```
/plugin marketplace add seon-biz/messy-middle
/plugin install messy-middle@seoncoder
```

## 사용법

설치 후 Claude Code에 이렇게 말하면 됩니다.

- "내 상세페이지 진단해줘 — https://..."
- "우리 가게 마케팅 전체를 봐줘"
- "이 진단 결과로 개선 기획서 만들어줘"
- "전략 덱(슬라이드)으로 만들어줘"

결과물: 진단 리포트(md) / 개선 기획서(md) / 전략 덱(슬라이드 스펙 md + 완성 HTML).

## 구조

```
plugins/messy-middle/skills/messy-middle/
├── SKILL.md                     워크플로와 규칙
└── references/
    ├── knowledge.md             메시미들 운영 지식 (단일 근거)
    ├── intake.md                경우별 질문 세트 (상품/서비스 × 개별/카테고리/전체)
    ├── report-standards.md      진단·기획 문서 표준
    ├── deck-standards.md        전략 덱 표준
    └── design-template.md       덱 디자인 템플릿
```

## 출처

이 스킬의 프레임워크는 Google과 The Behavioural Architects가 공동 발간한 아래 공개 연구에 기반합니다. 원문은 Think with Google에서 검색해 무료로 받을 수 있습니다.

- 『Decoding Decisions: Making sense of the messy middle』 (2020)
- 『Decoding Decisions: Marketing in the messy middle』 (2023)

`references/knowledge.md`는 위 연구를 운영 목적으로 요약·재구성한 문서이며, `[원문]` 표시만 연구 내용이고 `[운영]` 표시는 제작자의 실무 지식입니다. 원문 보고서 자체는 저작권 보호 대상이므로 이 저장소에 포함하지 않습니다.

## 라이선스

학습과 본인 비즈니스 적용은 자유입니다. 재판매·강의 자료 재사용·재배포는 허용하지 않습니다. 자세한 내용은 [LICENSE.md](LICENSE.md).

---

<sub>made by [세온코더](https://seonbiz.com)</sub>
