## 테크니컬 GEO 기본 점검표

![테크니컬 GEO 기본 점검](../assets/images/page-heroes/halox-geo-06-01-technical-geo-checklist-hero.png)

테크니컬 GEO는 개발 체크리스트를 길게 만드는 일이 아닙니다. AI와 검색엔진이 페이지를 발견하고, 읽고, 해석하고, 답변 근거로 인용할 수 있는지 확인하는 작업입니다.

콘텐츠와 source를 보강했는데도 공식 URL이 citation으로 잡히지 않는다면 기술 조건을 봐야 합니다. HaloX의 사이트 진단도 SEO 점수만 보여주는 화면이 아니라 URL별 SEO/GEO 점수, 이슈 패널, Pages 테이블을 통해 개발/SEO/콘텐츠 작업을 나누는 기준입니다.

[TOC]

## 기술 점검은 네 단계로 본다

기술 이슈는 한꺼번에 보면 복잡합니다. 먼저 AI가 페이지를 만나는 순서대로 나눕니다.

| 단계 | 확인할 질문 | 대표 항목 |
|---|---|---|
| 발견 | URL을 찾을 수 있는가 | sitemap, 내부 링크, robots |
| 접근 | crawler가 막히지 않는가 | HTTP 상태, robots.txt, robots meta |
| 해석 | 본문과 구조를 읽을 수 있는가 | SSR/CSR, 제목, 메타, heading, schema |
| 인용 | 답변 근거 URL로 쓸 수 있는가 | canonical, 첫 답변, FAQ, 업데이트 날짜 |

## HaloX 사이트 진단에서 먼저 볼 것

Overview에서는 SEO/GEO/성능 점수와 진단 추이를 봅니다. 점수만 보고 끝내지 말고 어떤 URL이 어떤 문제를 갖는지 Pages와 Issues로 내려가야 합니다.

Pages 테이블에서는 핵심 랜딩, 블로그, 뉴스룸, 리포트 예시, 상품/지점 페이지를 구분합니다. 비브랜드 질문에서 빠지는 페이지가 기술적으로도 약하다면 콘텐츠 수정 전에 개발 티켓이 먼저입니다.

Issues에서는 치명/경고/권장 이슈를 실행 담당으로 나눕니다. robots나 HTTP 상태는 개발, 메타/heading은 SEO/콘텐츠, schema와 내부 링크는 개발과 콘텐츠가 함께 봅니다.

![테크니컬 GEO 점검 레이어](../assets/images/body-figures/halox-geo-06-01-technical-geo-checklist-stack-codex-only.png)

*테크니컬 GEO는 URL을 발견하고, 접근하고, 해석하고, 인용하는 흐름으로 나눠야 실행 티켓이 보인다.*

## 가상 기업 AcmeGEO 예시

AcmeGEO의 리포트 예시 페이지는 내용이 충분하지만 “GEO 리포트 도구 추천” 질문에서 공식 URL citation이 생기지 않습니다. 사이트 진단을 보니 해당 URL은 sitemap에 늦게 반영되고, canonical이 다른 페이지를 가리키며, 첫 화면의 핵심 답변이 JavaScript 렌더링 뒤에야 나타납니다.

이 경우 콘텐츠를 더 쓰는 것보다 sitemap/canonical/렌더링 문제를 먼저 고칩니다. 수정 뒤에는 같은 질문 세트로 공식 URL citation이 회복되는지 확인합니다.

## 정리 양식

```text
점검 URL:
연결된 질문군:
발견 이슈:
접근 이슈:
해석 이슈:
인용 이슈:
개발 티켓:
콘텐츠/SEO 티켓:
재측정 질문:
```

## 다음 흐름

기본 점검 뒤에는 페이지 본문이 초기 HTML과 렌더링 후 DOM에서 어떻게 보이는지 확인해야 합니다. 이어서 [CSR/SSR 렌더링과 GEO 크롤링 리스크](https://wikidocs.net/346354)를 봅니다.
