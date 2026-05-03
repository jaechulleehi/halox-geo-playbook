## SEO 메타 정보와 canonical/robots meta 점검

![메타 정보 실전 점검](../assets/images/page-heroes/halox-geo-06-08-meta-canonical-snippet-checklist-hero.png)

메타 정보는 검색결과와 AI 답변 후보 URL의 기본 설명서입니다. title과 meta description은 페이지의 약속을 보여주고, canonical은 대표 URL을 정하며, robots meta는 색인 허용 여부를 알려줍니다.

GEO에서는 메타 정보가 본문 첫 답변, H2, 내부 링크와 같은 방향을 가리키는지 봐야 합니다.

[TOC]

## 실제로는 이렇게 보인다

```html
<head>
  <title>GEO 리포트 예시 | AcmeGEO</title>
  <meta name="description" content="브랜드 언급률, 답변 근거, 화면 인용을 나눠 읽는 GEO 리포트 예시입니다.">
  <link rel="canonical" href="https://example.com/ko/geo-report-sample">
  <meta name="robots" content="index,follow">
</head>
```

이 네 줄은 페이지의 대표 신호입니다. 본문이 다른 이야기를 하면 검색결과와 AI 답변 모두에서 해석이 흔들릴 수 있습니다.

## 항목별 점검 기준

| 항목 | 확인 질문 |
|---|---|
| title | 대표 질문과 핵심 키워드가 보이는가 |
| meta description | 클릭 전 기대와 본문 답변이 맞는가 |
| canonical | 대표 URL이 올바른가 |
| robots meta | 색인을 막고 있지 않은가 |

## canonical과 robots를 함께 본다

canonical이 잘못되면 좋은 페이지가 다른 URL의 신호로 합쳐질 수 있습니다. robots meta가 noindex라면 citation 후보가 되기 어렵습니다. 둘은 단순 태그가 아니라 URL 대표성과 접근성의 핵심 신호입니다.

![메타 정보와 citation 후보 URL 점검](../assets/images/body-figures/halox-geo-06-08-meta-canonical-snippet-control-panel-codex-only.png)

*메타 정보는 페이지가 어떤 질문의 대표 URL인지 알려주는 기본 신호다.*

## 실무 점검 순서

1. title이 실제 질문과 맞는지 본다.
2. description이 본문 첫 답변과 맞는지 본다.
3. canonical이 대표 URL을 가리키는지 확인한다.
4. robots meta가 index/follow인지 확인한다.
5. 검색 스니펫과 AI 답변 문맥을 함께 기록한다.

## 정리 양식

```text
URL:
title:
meta description:
canonical:
robots meta:
본문 첫 답변과의 일치 여부:
수정 액션:
재점검 날짜:
```

## 다음 흐름

메타 정보를 확인했다면 [사이트링크와 리치 리절트 차이](https://wikidocs.net/346857)에서 검색결과의 섹션 노출과 구조화 결과를 구분합니다.
