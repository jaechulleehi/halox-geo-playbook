## Schema 타입별 실전 점검표: Organization/Person/FAQ/Product

![Schema 타입별 실전 점검표: Organization/Person/FAQ/Product 대표 이미지](../assets/images/page-heroes/halox-geo-06-07-schema-type-checklist-hero.png)

Schema는 페이지에 숨겨 두는 SEO 장식이 아닙니다. Google은 구조화 데이터를 페이지 콘텐츠를 이해하는 데 활용한다고 설명합니다. schema.org는 `Organization`을 학교, 회사, 단체 같은 조직 유형으로 정의하고, `FAQPage`를 하나 이상의 자주 묻는 질문과 답을 제시하는 웹페이지 유형으로 정의합니다. Google 문서에서도 Organization 마크업은 주소, 연락처, 식별자 같은 조직의 관리 정보를 알려 주는 용도로, FAQ 구조화 데이터는 사용자가 자주 묻는 정보를 리치 결과로 발견하도록 돕는 용도로 설명합니다.

GEO 관점에서 중요한 질문은 “schema를 넣었는가”가 아닙니다. 더 중요한 질문은 “본문에 보이는 사실, HTML 텍스트, JSON-LD schema, title, canonical, 내부 링크가 같은 대상을 같은 의미로 설명하는가”입니다. 이 페이지는 Organization schema, Person/ProfilePage schema, FAQPage schema, Product schema를 실제로 어떻게 생겼는지 보고, 어떤 페이지에 어떤 타입을 써야 하는지 점검하는 실무 표입니다.

[TOC]

## schema는 실제로 어떻게 생겼나

가장 많이 쓰는 방식은 JSON-LD입니다. HTML의 `<script type="application/ld+json">` 안에 페이지의 구조화 정보를 넣습니다. 아래 예시는 형식을 이해하기 위한 축약 예시입니다. 실제 적용 전에는 Google 공식 문서와 schema.org 속성을 확인해야 합니다.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "HaloX Labs",
  "url": "https://haloxlabs.ai/",
  "logo": "https://haloxlabs.ai/logo.png",
  "sameAs": [
    "https://www.linkedin.com/company/example"
  ],
  "description": "AI 검색에서 브랜드 가시성을 분석하는 플랫폼"
}
</script>
```

이 코드가 의미 있으려면 화면 본문에도 같은 조직명, 서비스 설명, 공식 URL, 프로필 링크가 보여야 합니다. schema에만 멋진 설명을 넣고 본문에서는 다른 포지셔닝을 말하면 AI와 검색엔진 모두 어떤 설명을 믿어야 할지 흐려집니다.


## Organization/Person/FAQ/Product를 구분하는 빠른 기준

![Schema 타입 선택 기준표](../assets/images/body-figures/halox-geo-06-07-schema-type-selector-codex-only.png)

_schema 타입은 많이 넣는 것이 아니라 페이지 본문에 있는 정보와 역할에 맞춰 고르는 것입니다._


Schema 타입은 키워드가 아니라 페이지가 실제로 설명하는 대상에 맞춰 고릅니다. 회사 설명은 Organization, 사람/저자/전문가 설명은 Person/ProfilePage, 질문과 답변 묶음은 FAQPage, 상품/제품/소프트웨어 설명은 Product 또는 SoftwareApplication이 우선 후보입니다.

| 질문 | 우선 타입 | 잘못 고르면 생기는 문제 |
|---|---|---|
| 이 페이지가 회사/브랜드 자체를 설명하는가 | Organization | 제품 설명과 회사 설명이 섞임 |
| 이 페이지가 대표/전문가/저자를 설명하는가 | Person/ProfilePage | 조직 신호와 개인 전문성 신호가 섞임 |
| 이 페이지에 실제 FAQ가 보이는가 | FAQPage | 본문에 없는 질문을 schema에만 넣게 됨 |
| 이 페이지가 구매/도입 가능한 제품을 설명하는가 | Product/SoftwareApplication | 가격/기능/대상 고객 정보가 구조화되지 않음 |
| 이 페이지가 글/가이드/뉴스인가 | Article/BlogPosting/NewsArticle | 발행일/작성자/본문 주제가 불명확함 |

## 타입별로 맡는 역할

| schema 타입 | 주로 쓰는 페이지 | 본문에 먼저 있어야 할 정보 | GEO에서 보는 이유 |
|---|---|---|---|
| Organization | 회사 소개, 제품 사이트, 뉴스룸, 문의 페이지 | 공식 조직명, 로고, URL, 연락처, 소셜 프로필, 사업 설명 | 브랜드/entity를 같은 이름과 설명으로 묶기 위해 |
| Person | 대표/전문가/저자 소개, 인터뷰, 칼럼 저자 페이지 | 이름, 직함, 전문 분야, 소속, 프로필 URL, 예시로 쓸 수 있는 이력 | 누가 말하는지, 어떤 전문성을 가진 사람인지 설명하기 위해 |
| ProfilePage | 사람이나 조직의 상세 프로필 페이지 | 해당 인물/조직을 설명하는 본문과 관련 링크 | Google이 사람/조직 프로필 정보를 이해하도록 돕기 위해 |
| Article/BlogPosting | 블로그, 가이드, 뉴스룸 글 | 제목, 작성자, 게시일, 수정일, 본문 요약, 대표 이미지 | 글의 주제와 발행 정보를 안정적으로 전달하기 위해 |
| FAQPage | 실제 FAQ가 있는 페이지 | 질문과 답변이 화면 본문에 그대로 존재 | 질문/답의 짝을 분명히 만들어 AI 답변 재료로 쓰기 위해 |
| Product | 제품/상품 상세 페이지 | 상품명, 브랜드, 이미지, 가격, 재고, 리뷰, 정책 | 상품 비교/추천/구매 판단에 필요한 정보를 구조화하기 위해 |
| BreadcrumbList | 허브/카테고리/상세 페이지 | 상위 카테고리와 현재 페이지 위치 | 사이트 안에서 이 페이지가 어디에 속하는지 알려 주기 위해 |
| LocalBusiness | 병원/매장/지점/전문 서비스 | 이름, 주소, 전화번호, 영업시간, 예약 링크, 후기 정책 | 지역 질문과 방문 전환 질문에서 신뢰 기준을 만들기 위해 |

## Organization schema 점검

Organization schema는 “우리 회사가 무엇인지”를 검색엔진과 AI가 일관되게 이해하게 돕습니다. Google은 조직 마크업을 통해 주소, 연락처, 사업자 식별자 같은 관리 정보를 알려 줄 수 있다고 설명합니다.

| 확인 항목 | 좋은 상태 | 위험한 상태 |
|---|---|---|
| name | 공식 회사명과 본문 표기가 일치 | 서비스명, 법인명, 브랜드명이 섞여 있음 |
| url | 대표 도메인이 canonical과 일치 | 예전 도메인이나 캠페인 URL이 들어감 |
| logo | 현재 사용 중인 로고 URL | 깨진 이미지나 오래된 로고 |
| sameAs | 공식 SNS/프로필/디렉터리 링크 | 비공식 계정이나 오래된 프로필 |
| description | 본문 첫 설명과 같은 포지셔닝 | schema 설명만 과장되거나 다른 업종으로 남음 |
| contactPoint | 예시로 쓸 수 있는 연락처/문의 채널 | 내부 연락처나 더 이상 쓰지 않는 번호 |

GEO에서는 Organization schema를 단독으로 보지 않습니다. 회사 소개 페이지, 제품 페이지, 뉴스룸, 외부 프로필, 보도자료의 이름과 설명이 함께 맞아야 브랜드 합의 신호가 강해집니다.

## Person/ProfilePage schema와 바이오 정보

로이드가 말한 “바이오정보 schema”는 보통 사람 소개나 전문가 프로필을 구조화하는 영역입니다. schema.org에서는 `Person` 타입으로 사람의 이름, 소속, 직함, URL, 소개 정보를 표현할 수 있고, Google은 `ProfilePage` 구조화 데이터를 사람과 조직의 프로필 정보를 제공하는 데 쓸 수 있다고 안내합니다.

| 확인 항목 | 좋은 상태 | 위험한 상태 |
|---|---|---|
| name | 공개 프로필의 이름과 동일 | 별칭/영문명/한글명이 페이지마다 다름 |
| jobTitle | 현재 역할이 분명함 | 이전 직함이나 과장된 표현이 남음 |
| affiliation/worksFor | 소속 조직과 공식 페이지가 연결됨 | 소속 정보가 본문과 다름 |
| knowsAbout | 전문 분야가 본문 이력과 맞음 | 키워드만 나열하고 근거가 없음 |
| sameAs/url | LinkedIn, 공식 프로필, 저자 페이지 등 공개 링크 | 검증되지 않은 링크나 개인 계정 노출 |
| description | 본문 바이오와 같은 톤으로 요약 | schema에만 긴 홍보 문구가 있음 |

인물/전문가 페이지에서는 E-E-A-T를 흉내 내는 문구보다 예시로 쓸 수 있는 이력, 저자 페이지, 실제 작성 글, 인터뷰, 발표 자료 같은 연결 근거를 봐야 합니다. 의료/금융/법률처럼 규제가 있는 업종은 자격, 경력, 후기 표현이 법적 기준과 충돌하지 않는지도 함께 봐야 합니다.

## FAQPage schema 점검

FAQPage schema는 본문에 실제 질문과 답변이 있을 때만 의미가 있습니다. Google의 FAQ 문서는 구조화 데이터를 사용하면 사용자가 리치 결과에서 정보를 발견하는 데 도움이 될 수 있다고 설명하지만, schema를 넣는다고 노출이 보장되는 것은 아닙니다.

| 확인 항목 | 좋은 상태 | 위험한 상태 |
|---|---|---|
| 질문 | 독자가 실제로 묻는 질문 | 키워드만 바꾼 유사 질문 반복 |
| 답변 | 본문과 같은 답을 짧게 정리 | schema 답변이 본문보다 과장됨 |
| 개수 | 핵심 질문 3~6개 정도로 압축 | 페이지와 무관한 FAQ를 많이 넣음 |
| 위치 | 화면 본문에서 질문과 답이 보임 | JSON-LD에만 있고 사용자는 볼 수 없음 |
| 업데이트 | 정책/가격/기능 변경 때 함께 수정 | 오래된 답변이 schema에만 남음 |

GEO에서는 FAQ가 질문셋과 직접 연결됩니다. `GEO 비용은 얼마인가`, `GEO와 SEO는 무엇이 다른가`, `AI 검색 리포트는 어떻게 읽는가`처럼 실제 질문으로 들어오는 표현을 본문 FAQ와 schema가 같은 방식으로 답해야 합니다.

## Product schema 점검

Product schema는 커머스 GEO와 AI 구매 에이전트 대응에서 특히 먼저 봐야 합니다. Google은 상품 구조화 데이터가 검색 중인 잠재 구매자에게 상품 정보를 더 잘 보여 주는 데 도움이 될 수 있다고 설명합니다. 다만 실제 구매 판단에서는 Product schema, 상세페이지, merchant feed, 배송/반품 정책이 함께 맞아야 합니다.

| 확인 항목 | 좋은 상태 | 위험한 상태 |
|---|---|---|
| name/brand | 상품명과 브랜드가 상세페이지/feed와 일치 | 옵션명, 광고명, feed명이 서로 다름 |
| image | 현재 상품 이미지와 일치 | 품절/구버전 이미지가 남음 |
| offers.price | 최종 가격/할인가 기준이 명확 | 배너 가격, 장바구니 가격, schema 가격이 다름 |
| offers.availability | 재고/품절/예약판매 상태가 맞음 | 품절 상품이 구매 가능으로 표시됨 |
| aggregateRating/review | 리뷰 수와 평점이 실제 후기와 일치 | 리뷰를 과장하거나 검증되지 않은 평점 사용 |
| shipping/return | 배송/반품 정책과 연결 | 정책 페이지와 상품 단위 조건이 다름 |

Product schema는 [11-03. Product schema와 merchant feed 점검법](https://wikidocs.net/346599)에서 더 깊게 봅니다. 6장에서는 모든 페이지 유형에 공통으로 적용되는 기술 검수 원칙을 먼저 잡고, 11장에서는 커머스 운영 데이터와 feed 충돌까지 확장합니다.

## JSON-LD 예시로 보는 FAQPage

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "GEO와 SEO는 무엇이 다른가요?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "SEO는 검색 결과에서 발견되고 클릭될 수 있게 만드는 작업이고, GEO는 ChatGPT, Perplexity, Google AI Overviews 같은 AI 답변 환경에서 브랜드가 언급되고 답변 근거로 선택될 수 있게 만드는 작업입니다."
      }
    }
  ]
}
</script>
```

이 FAQ가 좋은 상태가 되려면 같은 질문과 답이 페이지 본문에도 보여야 합니다. JSON-LD만 넣고 화면에는 FAQ가 없다면 구조화 데이터와 사용자 경험이 어긋납니다.


## JSON-LD 예시로 보는 Product/SoftwareApplication

B2B SaaS나 GEO 분석 도구처럼 소프트웨어를 설명하는 페이지에서는 Product와 SoftwareApplication을 함께 검토할 수 있습니다. 중요한 것은 가격, 기능, 대상, FAQ가 본문과 충돌하지 않는 것입니다.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "HaloX",
  "applicationCategory": "BusinessApplication",
  "operatingSystem": "Web",
  "description": "AI 검색에서 브랜드 언급, 답변 근거, 화면 인용을 분석하는 GEO 플랫폼",
  "publisher": {
    "@type": "Organization",
    "name": "HaloX Labs",
    "url": "https://haloxlabs.ai/"
  },
  "offers": {
    "@type": "Offer",
    "priceCurrency": "KRW",
    "availability": "https://schema.org/InStock"
  }
}
</script>
```

가격을 공개하지 않는 B2B 제품이라면 schema에 임의 가격을 넣지 않습니다. 본문에서 공개한 도입 방식, 문의 경로, 기능 설명과 충돌하지 않는 범위에서만 구조화합니다.

## 타입 선택 순서

1. 먼저 페이지 목적을 한 문장으로 씁니다.
2. 화면 본문에 실제로 있는 정보만 표시합니다.
3. 페이지 유형에 맞는 schema 후보를 고릅니다.
4. title, H2, canonical, 내부 링크와 같은 의미인지 확인합니다.
5. Rich Results Test와 Schema Markup Validator로 오류를 봅니다.
6. Search Console과 AI 질문셋 재측정으로 실제 노출/인용 변화를 확인합니다.

## schema 타입 선택을 fan-out 노드와 연결하기

schema 타입은 페이지 모양이 아니라 AI가 확인하는 fan-out 노드에 맞춰 선택해야 합니다.

| fan-out 노드 | 우선 schema 후보 | 확인할 본문 정보 |
|---|---|---|
| entity 확인 | Organization, Person, ProfilePage | 이름, URL, logo, sameAs, 대표 설명 |
| 정의/가이드 | Article, FAQPage | 정의, 범위, FAQ, 업데이트 날짜 |
| 비교/추천 | Product, SoftwareApplication, Review 후보 | 기능, 대상 고객, 가격/조건, 비교 기준 |
| 실행 | HowTo 후보, Article | 단계, 도구, 완료 기준 |
| 리스크/정책 | FAQPage, Article | 주의사항, 적용 범위, 최신 정책 |

본문에 없는 정보를 schema에만 넣으면 신뢰 신호가 아니라 리스크입니다. schema는 4장에서 만든 답변 구조를 기술적으로 표시하는 보조 장치입니다.

## URL별 schema 점검표

| URL | 페이지 유형 | 우선 schema | 본문 확인 | 기술 확인 | 완료 기준 |
|---|---|---|---|---|---|
| 회사 소개 | Organization, ProfilePage | 조직명/설명/로고/공식 링크 | 본문과 JSON-LD 대조 | 공식 이름과 설명이 일치 |
| 대표/전문가 프로필 | Person, ProfilePage | 이름/직함/전문 분야/소속 | 프로필 URL과 sameAs 확인 | 예시로 쓸 수 있는 이력만 구조화 |
| 블로그/가이드 | Article, FAQPage, BreadcrumbList | 제목/작성일/FAQ/본문 요약 | Rich Results Test 확인 | 본문과 FAQ schema 일치 |
| 제품/SaaS 페이지 | Product 또는 SoftwareApplication, FAQPage | 기능/대상/가격/FAQ | canonical/title/schema 대조 | 제품 설명과 가격 기준 일치 |
| 커머스 상품 | Product, Offer, Review, BreadcrumbList | 가격/재고/리뷰/배송/반품 | feed와 schema 대조 | 구매 조건 충돌 없음 |
| 로컬 지점 | LocalBusiness, FAQPage, Review | NAP/영업시간/예약/후기 | 지도 프로필과 본문 대조 | 지역 질문과 방문 정보 일치 |

## 참고 링크

- Google Search Central: [구조화 데이터 소개](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data)
- Google Search Central: [Organization schema markup](https://developers.google.com/search/docs/appearance/structured-data/organization)
- Google Search Central: [ProfilePage schema markup](https://developers.google.com/search/docs/appearance/structured-data/profile-page)
- Google Search Central: [FAQ structured data](https://developers.google.com/search/docs/appearance/structured-data/faqpage)
- Google Search Central: [Product structured data](https://developers.google.com/search/docs/appearance/structured-data/product)
- schema.org: [Organization](https://schema.org/Organization), [Person](https://schema.org/Person), [FAQPage](https://schema.org/FAQPage), [Product](https://schema.org/Product)
- HaloX: [스키마 마크업 실전 가이드](https://haloxlabs.ai/ko/blog/schema-markup-practical), [스키마 마크업 용어집](https://haloxlabs.ai/ko/glossary/schema-markup)

## 흔한 질문

**Q. Organization schema만 넣으면 브랜드 entity가 잡히나요?**

아닙니다. Organization schema는 중요한 보조 신호지만, 회사 소개/제품 페이지/뉴스룸/외부 프로필/보도자료의 이름과 설명이 함께 맞아야 합니다.

**Q. Person schema에는 어느 정도까지 넣어야 하나요?**

예시로 쓸 수 있는 정보만 넣습니다. 이름, 직함, 소속, 전문 분야, 공식 프로필처럼 본문에 보이는 정보가 기준입니다. 민감한 개인정보나 검증되지 않은 경력은 넣지 않습니다.

**Q. FAQPage schema는 모든 글에 넣는 게 좋나요?**

아닙니다. 실제 FAQ가 있는 페이지에만 넣는 편이 좋습니다. 질문과 답이 본문에 없거나 페이지 목적과 무관하면 오히려 구조가 어색해집니다.

**Q. schema 오류가 없으면 GEO 성과가 좋아지나요?**

오류 없음은 출발점입니다. GEO에서는 여기에 본문 품질, 출처 신뢰도, 내부 링크, 질문셋 적합성, 실제 AI 답변의 mention/source/citation 변화를 함께 봐야 합니다.

## 다음 흐름

Schema 타입별 점검을 마쳤다면 [06-06. Google 공식 도구로 SEO/GEO 기술 상태 점검하기](https://wikidocs.net/346842)에서 Rich Results Test, Schema Markup Validator, PageSpeed, Search Console로 검증합니다. 커머스 상품 데이터는 [11-03. Product schema와 merchant feed 점검법](https://wikidocs.net/346599), 로컬/병원 지점 정보는 [12-02. NAP: 이름/주소/전화번호 일관성 점검](https://wikidocs.net/346608)과 함께 봅니다.
