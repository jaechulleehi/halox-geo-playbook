## 메타 정보 실전 점검: title/meta description/canonical/robots meta

메타 정보는 검색 결과에 보이는 문구만 고치는 작업이 아닙니다. GEO 관점에서는 “이 URL이 어떤 질문의 답인지”, “어느 URL을 대표로 봐야 하는지”, “검색엔진과 AI가 이 페이지를 읽고 따라가도 되는지”를 먼저 알려 주는 기술 신호입니다.

Google 문서에서는 title link가 검색 결과 제목으로 쓰일 수 있고, meta description은 검색 결과 설명 후보가 될 수 있으며, canonical은 중복 URL 중 대표 URL을 지정하는 방법이라고 설명합니다. robots meta tag는 색인과 링크 추적, 검색 결과 표시 방식을 페이지 단위로 조정하는 신호입니다.

[TOC]

## 메타 정보는 실제로 어떻게 생겼나

아래 예시는 실무에서 가장 먼저 확인하는 기본 형태입니다. 중요한 것은 코드가 있는지가 아니라, 본문 첫 문단과 같은 주제를 말하는지입니다.

```html
<head>
  <title>GEO 뜻: 생성형 엔진 최적화란 무엇인가 | HaloX</title>
  <meta name="description" content="GEO의 의미, SEO/AEO/AIO와의 차이, AI 검색에서 봐야 할 답변 근거와 화면 인용 기준을 정리합니다.">
  <link rel="canonical" href="https://haloxlabs.ai/ko/glossary/generative-engine-optimization">
  <meta name="robots" content="index,follow">
  <meta property="og:title" content="GEO 뜻: 생성형 엔진 최적화란 무엇인가">
  <meta property="og:description" content="AI 검색에서 브랜드가 언급되고 인용되도록 만드는 GEO 기본 개념을 설명합니다.">
</head>
```

이 코드에서 title은 페이지의 대표 질문을, description은 본문에서 얻는 답을, canonical은 대표 URL을, robots meta는 색인/링크 추적 허용 여부를 말합니다. 네 요소가 서로 다른 메시지를 주면 AI와 검색엔진은 페이지의 역할을 안정적으로 이해하기 어렵습니다.

## 항목별 점검 기준

| 항목 | Google 공식 문서에서 보는 역할 | GEO에서의 실무 기준 | 위험한 상태 |
|---|---|---|---|
| title | 검색 결과 제목 후보 | 핵심 질문/주제/브랜드가 자연스럽게 보임 | 모든 페이지가 같은 제목이거나 키워드만 나열 |
| meta description | 검색 결과 설명 후보 | 본문에서 실제로 답하는 내용을 1~2문장으로 요약 | 클릭 유도 문구만 있고 본문 내용과 다름 |
| canonical | 중복 URL 중 대표 URL 지정 | AI가 인용해야 할 대표 URL이 분명함 | 필터/추적/구 URL이 대표로 남음 |
| robots meta | 색인/링크 추적/스니펫 표시 제어 | 핵심 페이지가 index/follow 상태 | 중요한 페이지가 noindex/nofollow로 배포 |
| Open Graph | 공유 미리보기 제목/설명 | Slack/카카오/소셜 공유에서도 같은 메시지 유지 | SEO title과 공유 title이 다른 주제 |

## title을 쓸 때의 기준

Title은 “키워드 넣는 칸”이 아니라 페이지의 대표 질문을 압축하는 칸입니다. Google은 title link가 페이지의 제목 요소, 본문 제목, 링크 앵커 등 여러 신호를 참고해 생성될 수 있다고 설명합니다. 그러므로 title과 H1/H2/본문 첫 문단이 같은 주제를 말해야 합니다.

| 페이지 유형 | 좋은 title 예시 | 피해야 할 title |
|---|---|---|
| 용어 페이지 | GEO 뜻: 생성형 엔진 최적화란 무엇인가 | GEO, SEO, AEO, AIO, LLMO 총정리 |
| 제품 페이지 | AI 검색 브랜드 가시성 분석 플랫폼 HaloX | 최고의 GEO 솔루션 |
| 비교 페이지 | SEO 도구와 GEO 도구 비교: 무엇을 다르게 봐야 하나 | 도구 비교 |
| 병원/로컬 페이지 | 강남 피부과 여드름 상담 전 확인할 기준 | 강남 피부과 추천 1위 |

GEO에서는 title이 질문셋과 맞아야 합니다. “GEO 도구 비교” 페이지라면 도구 이름보다 비교 기준, 리포트 검증, 답변 근거 확인 같은 독자 질문이 보여야 합니다.

## meta description을 쓸 때의 기준

Meta description은 순위를 직접 올리는 마법 문장이 아닙니다. 하지만 검색 결과 설명 후보이자 페이지 목적을 압축하는 신호입니다. GEO에서는 AI가 페이지를 어떤 질문의 답으로 볼지 추론하는 데 도움이 되는 요약 문장으로 씁니다.

| 좋게 쓰는 법 | 나쁜 상태 |
|---|---|
| 본문이 실제로 제공하는 답을 쓴다 | 본문에 없는 약속을 쓴다 |
| 대상 독자와 사용 장면을 드러낸다 | “최고/완벽/혁신” 같은 홍보어만 쓴다 |
| 핵심 용어를 자연스럽게 1~2개 넣는다 | 키워드를 쉼표로 나열한다 |
| 페이지마다 다르게 작성한다 | 사이트 전체가 같은 description을 쓴다 |

예를 들어 `06-07 Schema 타입별 실전 점검표`라면 “Organization, Person/ProfilePage, FAQPage, Product schema가 실제로 어떻게 생겼는지 보고, 본문/HTML/JSON-LD 일치 기준을 점검합니다”처럼 페이지의 산출물이 보여야 합니다.

## canonical과 robots meta를 함께 봐야 하는 이유

Canonical은 대표 URL을 알려 주고, robots meta는 해당 페이지를 색인하거나 링크를 따라가도 되는지 알려 줍니다. 둘 중 하나만 맞아도 충분하지 않습니다.

| 상황 | 겉보기 상태 | 실제 리스크 | 수정 기준 |
|---|---|---|---|
| canonical이 구 URL | 페이지는 열림 | AI가 오래된 URL을 source로 잡을 수 있음 | 새 대표 URL로 canonical 정리 |
| noindex가 남음 | 사용자는 접근 가능 | 검색/AI 발견 가능성이 낮아짐 | 공개 핵심 페이지는 index/follow 확인 |
| 추적 URL이 canonical | 캠페인 성과 측정은 됨 | 대표 URL이 분산됨 | 추적 파라미터 없는 대표 URL 지정 |
| hreflang/canonical 충돌 | 언어별 페이지가 있음 | 글로벌 GEO 답변이 언어별로 흔들림 | 언어별 대표 URL과 관계 정리 |

## 실무 점검 순서

1. 핵심 질문셋에서 인용되어야 할 URL 20개를 고릅니다.
2. 각 URL의 title, meta description, canonical, robots meta를 뽑습니다.
3. 본문 첫 문단/H2/FAQ/schema가 같은 주제를 말하는지 비교합니다.
4. 중복 title, 빈 description, 잘못된 canonical, noindex를 표시합니다.
5. 수정 후 Search Console URL 검사와 AI 질문셋 재측정으로 변화를 봅니다.

## URL별 메타 점검표

| URL | 페이지 목적 | title 상태 | description 상태 | canonical 상태 | robots meta | GEO 영향 | 수정 액션 |
|---|---|---|---|---|---|---|---|
| 글로서리 | GEO 뜻 정의 | 질문형 title 있음 | 본문 요약 부족 | 정상 | index/follow | 정의 source 후보 약함 | description 보강 |
| 제품 페이지 | 브랜드 가시성 분석 소개 | 브랜드명만 있음 | 기능 나열 | 정상 | index/follow | 어떤 질문의 답인지 흐림 | title을 문제/대상 중심으로 수정 |
| 캠페인 URL | 리포트 다운로드 | 추적 URL title | canonical 없음 | 추적 URL | index/follow | citation 분산 | 대표 랜딩으로 canonical 지정 |
| 이전 블로그 | 구 URL | 오래된 title | 오래된 설명 | 구 URL | index/follow | 오래된 source 유지 | 301/canonical/본문 업데이트 |

## 참고 링크

- Google Search Central: [title link 문서](https://developers.google.com/search/docs/appearance/title-link)
- Google Search Central: [meta description/snippet 문서](https://developers.google.com/search/docs/appearance/snippet)
- Google Search Central: [canonical 지정 문서](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls)
- Google Search Central: [robots meta tag 문서](https://developers.google.com/search/docs/crawling-indexing/robots-meta-tag)
- HaloX: [온페이지 SEO 체크리스트](https://haloxlabs.ai/ko/blog/on-page-seo-checklist-2026)

## 흔한 질문

**Q. meta description을 잘 쓰면 AI 답변에 바로 나오나요?**

아닙니다. meta description은 보조 신호입니다. 본문 첫 문단, FAQ, 표, schema, 외부 출처가 함께 맞아야 AI 답변 근거로 쓰일 가능성이 커집니다.

**Q. canonical은 SEO 문제 아닌가요?**

SEO 문제이면서 GEO 문제입니다. AI가 답변 근거로 인용해야 할 대표 URL이 흔들리면 source/citation도 흔들릴 수 있습니다.

**Q. Open Graph도 GEO에 중요한가요?**

직접적인 검색 구조화 신호라기보다 공유/확산 문맥에서 중요합니다. Slack, 커뮤니티, SNS에서 공유될 때 제목과 설명이 본문과 맞아야 외부 언급과 브랜드 설명이 일관됩니다.

## 다음 흐름

메타 정보 점검까지 끝나면 6장 기술 점검은 `발견 가능성 → 렌더링 → URL 안정성 → 크롤러 접근성 → schema/내부 링크 → 공식 도구 검증 → 메타/canonical → 사이트링크/리치 리절트 구분` 흐름으로 닫힙니다. 검색결과 아래 작은 링크와 구조화 데이터 리치 리절트를 구분해야 한다면 [06-09. 사이트링크와 리치 리절트 차이](https://wikidocs.net/346857)를 이어서 봅니다. 이후에는 [07. 산업별 GEO 전략](https://wikidocs.net/346335)으로 넘어가 업종별로 어떤 기술 요소를 우선해야 하는지 봅니다.
