## Product schema와 merchant feed 점검법

![Product schema와 merchant feed 점검 흐름](../assets/images/page-heroes/halox-geo-11-03-product-schema-merchant-feed-hero.png)

Product schema와 merchant feed는 AI가 상품을 이해하도록 돕는 중요한 재료입니다. 다만 둘 중 하나만 넣는다고 커머스 GEO가 끝나지는 않습니다. schema, feed, HTML 본문, 정책 문서, 내부 링크가 서로 같은 의미를 가리켜야 합니다.

[Schema와 내부 링크](https://wikidocs.net/346394)에서 본 것처럼 schema는 본문을 대체하지 않습니다. 커머스에서는 이 원칙이 더 중요합니다. 가격, 재고, 옵션, 배송, 반품처럼 실제 거래에 영향을 주는 정보가 서로 다르면 AI는 무엇을 믿어야 할지 판단하기 어렵습니다.

[TOC]

## Product schema가 보완하는 것

Product schema는 상품 페이지의 핵심 정보를 구조화된 형식으로 전달합니다. 검색 엔진과 AI 시스템이 상품명, 브랜드, 이미지, SKU, 가격, 재고, 리뷰, 평점 등을 더 안정적으로 이해하는 데 도움이 됩니다.

| schema 항목 | 확인할 질문 | 본문과 맞춰 볼 지점 |
|---|---|---|
| `name` / `brand` | 상품명과 브랜드명이 일관적인가 | 제목, H2, 상품명 표기, feed 상품명 |
| `sku` / `gtin` | 상품 식별자가 있는가 | 옵션별 SKU, 모델명, 바코드, 내부 상품 ID |
| `offers` | 가격과 구매 가능 상태가 맞는가 | 최종가, 할인가, 재고, 품절, 예약판매 |
| `aggregateRating` / `review` | 리뷰 신호가 과장 없이 연결되는가 | 리뷰 수, 평점, 최신성, 구매 인증 |
| `shippingDetails` | 배송 조건을 설명할 수 있는가 | 배송 지역, 배송비, 예상 도착일, 무료배송 조건 |
| `hasMerchantReturnPolicy` | 반품 조건이 명확한가 | 반품 기간, 제외 조건, 배송비 부담, 환불 방식 |

schema가 비어 있으면 AI가 상품을 이해하는 데 불리할 수 있습니다. 하지만 schema가 본문과 다르면 더 큰 문제가 됩니다. 구조화 데이터는 `숨겨진 정답지`가 아니라 페이지가 말하는 내용을 확인해 주는 보조 신호입니다.

## Product schema는 어떻게 생겼나

아래는 개념을 이해하기 위한 단순 예시입니다. 실제 운영에서는 Google의 [Product structured data](https://developers.google.com/search/docs/appearance/structured-data/product)와 schema.org의 [Product](https://schema.org/Product), [Offer](https://schema.org/Offer)를 확인하고, 페이지 본문에 보이는 정보와 맞춰야 합니다.

```json
{
  "@context": "https://schema.org/",
  "@type": "Product",
  "name": "Acme Quiet Headphone 300",
  "image": ["https://example.com/images/headphone-300.jpg"],
  "description": "노이즈 캔슬링을 지원하는 250g 블루투스 헤드폰입니다.",
  "sku": "ACME-HP-300-BK",
  "gtin13": "8801234567890",
  "brand": {
    "@type": "Brand",
    "name": "Acme"
  },
  "offers": {
    "@type": "Offer",
    "url": "https://example.com/products/headphone-300",
    "priceCurrency": "KRW",
    "price": "179000",
    "availability": "https://schema.org/InStock",
    "itemCondition": "https://schema.org/NewCondition"
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.7",
    "reviewCount": "320"
  }
}
```

이 예시에서 중요한 것은 코드 자체가 아니라 값의 일치입니다. 상품명, 가격, 재고, 리뷰 수가 본문/장바구니/feed/정책 문서와 다르면 오히려 혼란을 만듭니다.

## merchant feed가 보완하는 것

merchant feed는 상품 목록과 가격, 재고, URL, 이미지, 카테고리 정보를 플랫폼에 전달하는 데이터 흐름입니다. 커머스에서는 상품 수가 많고 정보가 자주 바뀌기 때문에 페이지 본문만으로 최신 상태를 설명하기 어렵습니다.

| feed 항목 | 왜 중요한가 | 충돌 위험 |
|---|---|---|
| `id` / `item_group_id` | 상품과 옵션을 구분합니다 | 같은 옵션이 다른 상품처럼 보임 |
| `title` | 상품을 검색/추천 단위로 묶습니다 | 페이지 제목과 feed 제목 불일치 |
| `price` / `sale_price` | 실제 결제 조건을 판단합니다 | 배너 가격, 장바구니 가격, feed 가격 충돌 |
| `availability` | 구매 가능 여부를 판단합니다 | 품절 상품 추천 |
| `link` / canonical | 어떤 URL을 기준으로 볼지 정합니다 | 중복 URL, 추적 URL, 잘못된 canonical |
| `shipping` / returns | 배송과 반품 조건을 판단합니다 | 정책 페이지와 feed 조건 충돌 |

feed는 실시간에 가까운 운영 데이터와 연결됩니다. 그래서 커머스 GEO에서는 콘텐츠팀만이 아니라 MD, 개발, 운영, CS, 광고 담당자가 함께 봐야 합니다.

## schema와 feed의 역할 차이

| 구분 | Product schema | merchant feed |
|---|---|---|
| 위치 | 상품 상세페이지 HTML/JSON-LD | Merchant Center 또는 플랫폼 데이터 피드 |
| 강점 | 페이지의 의미와 구조를 설명 | 대량 상품의 최신 운영 값을 전달 |
| 자주 바뀌는 값 | 가격/재고/리뷰가 바뀔 수 있음 | 가격/재고/배송/프로모션이 자주 바뀜 |
| 주요 담당 | 개발/SEO/콘텐츠 | MD/운영/광고/개발 |
| GEO 관점 | AI가 페이지 내용을 이해하는 보조 신호 | AI와 플랫폼이 최신 상품 상태를 판단하는 운영 신호 |
| 리스크 | 본문과 다른 schema | 페이지와 다른 feed |

둘 중 하나가 다른 하나를 대체하지 않습니다. 상세페이지 본문, Product schema, merchant feed, 정책 문서가 같은 상품을 같은 조건으로 설명해야 합니다.

## 함께 점검할 순서

1. 대표 상품 20개를 고릅니다. 매출 상위, 광고 집행, 반품/문의 많은 상품을 섞습니다.
2. 상세페이지의 상품명, 가격, 옵션, 재고, 배송, 반품 정보를 표로 적습니다.
3. Product schema의 값이 페이지 본문과 같은지 확인합니다.
4. merchant feed의 title, price, availability, link가 실제 구매 가능 상태와 맞는지 확인합니다.
5. 정책 문서의 배송/반품/환불 조건이 상품 단위로 연결되는지 봅니다.
6. AI 구매 질문을 던져 가격, 재고, 배송, 반품을 잘못 설명하는지 봅니다.
7. 충돌이 있는 항목부터 수정하고 같은 질문으로 재측정합니다.

## 정합성 점검표

| 점검 항목 | 상세페이지 | Product schema | merchant feed | 정책 문서 | 판정 |
|---|---|---|---|---|---|
| 상품명 |  |  |  |  | 일치/불일치 |
| 브랜드 |  |  |  |  | 일치/불일치 |
| SKU/GTIN |  |  |  |  | 일치/불일치 |
| 최종 가격 |  |  |  |  | 일치/불일치 |
| 할인 기간 |  |  |  |  | 일치/불일치 |
| 재고/품절 |  |  |  |  | 일치/불일치 |
| 배송비/도착 |  |  |  |  | 일치/불일치 |
| 반품 가능 기간 |  |  |  |  | 일치/불일치 |
| 대표 URL/canonical |  |  |  |  | 일치/불일치 |

## 공식 도구로 확인하기

| 확인 대상 | 도구/문서 | 확인할 것 |
|---|---|---|
| Product structured data | [Google Product structured data](https://developers.google.com/search/docs/appearance/structured-data/product) | 지원 속성, 리치 결과 요건, 권장 항목 |
| 리치 결과 가능성 | [Rich Results Test](https://search.google.com/test/rich-results) | 오류/경고, 본문과 schema 일치 여부 |
| schema 문법 | [Schema Markup Validator](https://validator.schema.org/) | JSON-LD 구조와 schema.org 타입 |
| merchant feed | [Merchant Center 제품 데이터 사양](https://support.google.com/merchants/answer/7052112) | id/title/price/availability/link/shipping 등 필수/권장 값 |
| 반품 정책 | [Google 반품 정책 structured data](https://developers.google.com/search/docs/appearance/structured-data/return-policy) | return policy 표현 가능 여부 |

공식 도구에서 오류가 없다고 해서 GEO가 끝난 것은 아닙니다. 오류 없음은 최소 조건이고, 실제 질문에 답할 수 있는 본문/표/정책 링크가 함께 있어야 합니다.

## 완료 기준

- 대표 상품 20개의 상세페이지/schema/feed/정책 문서 값을 비교했습니다.
- 가격/재고/배송/반품/URL 충돌 항목을 분리했습니다.
- Product schema가 본문에 없는 내용을 과장하지 않습니다.
- merchant feed가 실제 구매 가능 상태와 맞습니다.
- 같은 AI 구매 질문으로 수정 전후를 재측정할 수 있습니다.

## 참고 링크

구현 기준은 Google의 [Product structured data](https://developers.google.com/search/docs/appearance/structured-data/product)와 [Merchant Center 제품 데이터 사양](https://support.google.com/merchants/answer/7052112)을 참고할 수 있습니다. 개념 설명은 HaloX의 [스키마 마크업 실무 가이드](https://haloxlabs.ai/ko/blog/schema-markup-practical)와 [스키마 마크업 용어집](https://haloxlabs.ai/ko/glossary/schema-markup)을 함께 보면 좋습니다.

## 다음 흐름

다음 페이지에서는 커머스 GEO에서 실제로 위험한 가격/재고/배송/반품/리뷰/결제 오류를 2주 안에 어떻게 줄일지 정리합니다.
