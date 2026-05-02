## FAQ/표/schema는 언제 쓰는가

![FAQ와 표와 schema 구조화 흐름](../assets/images/page-heroes/halox-geo-04-02-faq-schema-table-structure-hero.png)

FAQ, 표, 리스트, schema는 글을 꾸미는 장식이 아니라 질문과 답변 재료를 구조화하는 도구입니다. 표는 비교 기준을 보존하고, FAQ는 질문과 짧은 답의 짝을 보존하며, schema는 본문에 이미 있는 정보를 검색엔진이 이해하기 쉬운 형식으로 보조합니다.

가장 중요한 원칙은 `본문 먼저, 구조화는 그 다음`입니다. 본문에 없는 정보를 schema에만 넣거나, 실제로 답하지 않는 질문을 FAQ로 억지로 만드는 것은 좋은 GEO 구조가 아닙니다. 독자 화면, HTML 본문, 내부 링크, schema가 같은 사실을 말해야 합니다.

[TOC]

## FAQ/표/schema의 역할 분리

| 도구 | 가장 잘 맞는 상황 | AI 답변에서 맡는 역할 | 조심할 점 |
|---|---|---|---|
| FAQ | 반복되는 짧은 질문과 답이 있을 때 | 후속 질문과 빠른 답을 제공 | 본문에 없는 내용을 FAQ에만 넣지 않음 |
| 표 | 여러 항목을 같은 기준으로 비교할 때 | 비교/추천 질문의 기준을 고정 | 기준이 불명확한 표는 오히려 혼란을 줌 |
| 리스트 | 순서나 체크 항목을 보여줄 때 | 실행 단계를 분리 | 긴 문단을 보기 좋게 쪼개는 용도로만 쓰지 않음 |
| schema | 페이지 유형과 핵심 정보를 보조할 때 | 구조화 데이터 신호 제공 | 리치 결과를 보장한다고 오해하지 않음 |
| 내부 링크 | 다음 질문으로 이어질 때 | 주제 간 관계를 설명 | 맥락 없는 링크 묶음을 피함 |

## 표가 중요한 진짜 이유

AI 답변은 여러 출처에서 기준을 뽑아 비교하고 요약하는 경우가 많습니다. 긴 문단은 기준과 값을 분리하기 어렵지만, 표는 `항목`, `기준`, `값`, `주의점`을 같은 구조로 묶어 줍니다.

| 문단만 있을 때 | 표로 정리했을 때 | GEO 효과 |
|---|---|---|
| 기준과 예시가 섞인다 | 기준/설명/확인 방법이 분리된다 | AI가 비교 질문에 답하기 쉽다 |
| 중요한 수치가 문장 속에 묻힌다 | 수치와 상태가 한 칸에 고정된다 | 답변 근거로 재사용하기 쉽다 |
| 여러 제품/URL 비교가 흐려진다 | 같은 열 기준으로 비교된다 | 경쟁 비교 문맥을 해석하기 쉽다 |
| 리라이트 후 변화가 모호하다 | 수정 전/후 항목이 남는다 | 재측정 리포트로 연결하기 쉽다 |

## schema는 무엇이고 어디까지 봐야 하나

Google은 구조화 데이터를 페이지 정보를 분류하기 위해 표준화된 형식으로 제공하는 데이터로 설명합니다. 보통 JSON-LD 형식으로 HTML 안에 넣고, 검색엔진이 페이지의 주제, 유형, 이름, 날짜, 질문/답변 같은 정보를 더 명확히 이해하도록 돕습니다.

하지만 schema는 본문을 대체하지 않습니다. Google의 [구조화 데이터 소개](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data)와 각 타입 문서에서도 구조화 데이터는 검색 기능과 리치 결과 이해를 돕는 방식으로 설명됩니다. schema를 넣었다고 리치 결과나 AI 인용이 보장되는 것은 아닙니다.

| 페이지 유형 | 본문에 먼저 있어야 할 것 | schema 후보 | 주의할 점 |
|---|---|---|---|
| 용어/가이드 | 정의, 범위, 예시, 관련 질문 | Article, FAQPage | 본문 없는 정의를 schema에만 넣지 않음 |
| 뉴스룸/보도자료 | 날짜, 조직명, 핵심 팩트, 관련 자료 | Article, NewsArticle, Organization | 조직명/제품명 표기가 흔들리지 않아야 함 |
| 제품/도구 | 기능, 대상, 가격/플랜, 비교 기준 | Product, SoftwareApplication, FAQPage | 오래된 가격/기능 설명이 남지 않게 함 |
| How-to | 단계, 조건, 완료 기준 | HowTo, Article, FAQPage | 실제 단계가 화면 본문에 보여야 함 |
| FAQ 페이지 | 실제 질문과 답변 | FAQPage | 질문/답변이 사용자 화면에 보여야 함 |

## FAQPage JSON-LD는 어떻게 생겼나

FAQPage schema는 페이지에 실제 질문과 답변이 있을 때 사용할 수 있습니다. 아래는 형태를 이해하기 위한 축약 예시입니다. 실제 적용은 Google의 [FAQ structured data 문서](https://developers.google.com/search/docs/appearance/structured-data/faqpage)와 [schema.org FAQPage](https://schema.org/FAQPage)를 함께 확인해야 합니다.

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "GEO 콘텐츠에 FAQ는 반드시 필요한가?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "반드시 필요한 것은 아니지만 반복 질문을 짧게 답하고 후속 질문을 정리할 때 유용합니다."
      }
    }
  ]
}
```

이 예시에서 중요한 것은 JSON-LD 자체가 아니라 `name`과 `acceptedAnswer.text`가 실제 페이지 본문에 보이는 질문/답변과 일치해야 한다는 점입니다.

## Article JSON-LD는 어떻게 생겼나

Article schema는 가이드, 블로그, 뉴스룸 글처럼 본문형 콘텐츠의 기본 정보를 설명할 때 사용할 수 있습니다. 아래는 개념 예시입니다.

```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "AI가 인용하는 Answer-first 콘텐츠는 어떻게 쓰는가",
  "description": "첫 답변, 표, FAQ, source를 활용해 AI가 읽기 좋은 콘텐츠 구조를 만드는 방법",
  "author": {
    "@type": "Organization",
    "name": "HaloX Labs"
  },
  "dateModified": "2026-04-30"
}
```

Article schema를 넣을 때도 headline, description, author, 날짜가 페이지 본문과 충돌하지 않아야 합니다. 자세한 기준은 Google의 [Article structured data 문서](https://developers.google.com/search/docs/appearance/structured-data/article)와 [schema.org Article](https://schema.org/Article)을 참고합니다.

## query 의도별 구조화 요소 매칭

FAQ, 표, schema는 페이지에 많이 넣는 것이 목표가 아닙니다. query 의도에 따라 어떤 구조화 요소가 가장 도움이 되는지 먼저 정해야 합니다.

| query 의도 | 우선 구조 | schema 후보 | 주의할 점 |
|---|---|---|---|
| 정의형 | 짧은 정의, 용어표, FAQ | Article, FAQPage | 본문 없는 FAQ만 만들지 않음 |
| 비교형 | 기준표, 장단점 표 | Article, Product 후보 | 기준이 같은 열로 비교되는지 확인 |
| 추천형 | 상황별 추천/제외 조건 | Article, Product, Review 후보 | 과장된 순위표처럼 보이지 않게 함 |
| 검증형 | 증빙 자료, source 목록, 체크리스트 | Article, Organization | 주장과 근거 URL을 분리하지 않음 |
| 실행형 | 순서 리스트, 워크시트, 완료 기준 | HowTo 후보 | 실제 실행 단계가 본문에 있어야 함 |
| 리스크형 | 금지 표현, 안전 문장, FAQ | FAQPage, Article | 법무/정책 검토가 필요한 문장 표시 |

이 매칭표를 쓰면 구조화가 장식이 아니라 답변 설계가 됩니다. 예를 들어 AcmeGEO 리포트 예시 페이지는 실행형/검증형이 섞여 있으므로, 리포트 항목 표와 FAQ를 먼저 만들고 본문에 있는 정보만 schema 후보로 넘기는 편이 안전합니다.

![FAQ 표 schema 선택 매트릭스](../assets/images/body-figures/halox-geo-04-02-faq-table-schema-matrix-codex-only.png)

_질문 의도에 따라 FAQ, 표, Article schema, FAQPage schema의 역할을 나누면 구조화가 장식이 아니라 답변 설계가 됩니다._

## 구조화 요소 선택 기준

| 상황 | 우선 쓸 구조 | 이유 |
|---|---|---|
| 같은 주제에 반복 질문이 많다 | FAQ | 질문/답변 쌍을 명확히 남김 |
| 여러 도구나 기준을 비교한다 | 표 | 비교 기준을 보존 |
| 순서대로 따라 해야 한다 | 리스트/체크리스트 | 실행 단계를 분리 |
| 페이지 유형을 명확히 알려야 한다 | schema | 본문 의미를 구조화 데이터로 보조 |
| 다음 질문으로 이어져야 한다 | 내부 링크 | 주제 관계와 탐색 흐름 제공 |
| 신뢰 근거가 필요하다 | source 링크 | 주장과 근거를 연결 |

## schema 사용 금지 패턴

| 금지 패턴 | 왜 문제인가 | 바른 방향 |
|---|---|---|
| 본문에 없는 답변을 FAQPage에만 넣음 | 사용자에게 보이지 않는 정보로 구조화 | 먼저 본문 FAQ를 작성한 뒤 schema 적용 |
| 오래된 가격/기능을 Product schema에 남김 | AI와 검색엔진이 잘못된 정보를 이해할 수 있음 | 본문과 schema를 함께 업데이트 |
| 모든 글에 같은 FAQ를 반복 | 중복/저품질 구조가 됨 | 페이지별 실제 후속 질문만 사용 |
| schema를 넣으면 AI 인용이 보장된다고 설명 | 과장된 약속 | 발견/이해를 돕는 보조 신호로 설명 |
| Organization/Person 정보를 페이지마다 다르게 표기 | 엔티티 신호가 흔들림 | 공식 표기 기준을 정하고 일관되게 사용 |


## 04장에서 구조화하고 05장으로 넘길 것

FAQ, 표, schema를 넣었다고 바로 source/citation 문제가 해결되지는 않습니다. 04-02에서는 페이지 안의 정보 단위를 정리하고, 05장에서는 그 정보가 외부 근거와 브랜드 엔터티 신호로 이어지는지 봅니다.

| 04-02에서 만든 구조 | 05장에서 확인할 것 |
|---|---|
| FAQ | 같은 질문이 외부 리뷰/커뮤니티/뉴스룸에서도 같은 의미로 설명되는가 |
| 비교표 | 경쟁사와 비교될 때 우리 기준이 source로 쓰일 만큼 명확한가 |
| Article schema 후보 | 작성자/게시자/날짜/제목이 뉴스룸이나 외부 기사와 충돌하지 않는가 |
| FAQPage schema 후보 | 실제 화면 본문과 같은 질문/답변인지, 오래된 답이 아닌지 |
| Organization/Person 언급 | 공식명, 대표자, 제품명, `sameAs` 외부 프로필이 일관되는가 |
| 내부 링크 | 다음 질문뿐 아니라 대표 source URL과도 연결되는가 |

## 실습 워크시트

| 입력 항목 | 작성 기준 |
|---|---|
| 목표 질문 | 이 페이지가 답할 핵심 질문 |
| 표 후보 | 비교 기준/항목/주의점 |
| FAQ 후보 | 실제 후속 질문 3~5개 |
| schema 후보 | Article/FAQPage/Product/Organization 등 |
| 본문 일치 여부 | schema 내용이 화면 본문과 같은가 |
| 검증 위치 | 06장 기술 점검으로 넘길 URL |

## HaloX로 이어지는 지점

FAQ, 표, schema를 언제 써야 할지 감을 잡기 어렵다면 HaloX의 [AI 검색이 선택하는 콘텐츠 구조](https://haloxlabs.ai/ko/blog/ai-preferred-content-structure)와 [GEO 콘텐츠 구조화 가이드](https://haloxlabs.ai/ko/blog/geo-content-structure)를 함께 읽습니다. 이 페이지의 체크리스트로 배치 기준을 정하고, HaloX 글에서 AI가 선호하는 정보 단위의 예시를 확인합니다.

## 흔한 질문

**Q. 모든 페이지에 FAQPage schema를 넣어야 하나요?**

아닙니다. 실제 질문과 답변이 본문에 있는 페이지에만 검토합니다. FAQ가 억지라면 schema도 억지입니다.

**Q. schema를 넣으면 Google AI Overviews나 AI 답변에 바로 인용되나요?**

보장되지 않습니다. schema는 페이지 이해를 돕는 보조 신호입니다. 본문 품질, 출처, 링크, 검색 노출, 사용자에게 도움이 되는 내용이 함께 필요합니다.

**Q. 표와 FAQ 중 무엇을 먼저 써야 하나요?**

비교 기준이 중요하면 표를 먼저 씁니다. 반복 질문과 짧은 답이 중요하면 FAQ를 씁니다. 둘 다 필요하면 표로 기준을 고정하고 FAQ로 후속 질문을 받습니다.

## 다음 흐름

이전: [04-01. AI가 인용하는 Answer-first 콘텐츠는 어떻게 쓰는가](https://wikidocs.net/346347) / 다음: [04-03. 기존 글을 GEO 콘텐츠로 리라이트하는 체크리스트](https://wikidocs.net/346349)
