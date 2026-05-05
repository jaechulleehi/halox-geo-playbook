## Product schema와 merchant feed 점검

![Product schema와 merchant feed 점검](../assets/images/page-heroes/halox-geo-11-03-product-schema-merchant-feed-hero.png)

Product schema와 merchant feed는 커머스 GEO에서 AI와 검색엔진이 상품을 확인하는 중요한 데이터 층입니다. 문제는 둘 중 하나만 맞아서는 부족하다는 점입니다. 상세 페이지, schema, feed, 실제 결제 가능 상태가 서로 맞아야 추천 후보로 안정적으로 남습니다.

이 페이지의 목적은 schema를 많이 넣는 것이 아니라, 구매 질문에 필요한 정보가 같은 값으로 반복되는지 확인하는 것입니다.

[TOC]

## schema와 feed는 역할이 다르다

Product schema는 페이지 안의 상품 정보를 구조화해 검색엔진과 AI가 읽기 쉽게 돕습니다. merchant feed는 판매 가능 상태, 가격, 재고, 배송 같은 상거래 정보를 플랫폼에 전달합니다. 둘은 겹치지만 같은 것이 아닙니다.

예를 들어 상세 페이지에는 89,000원, schema에는 99,000원, feed에는 품절로 표시되어 있다면 AI가 어떤 값을 믿어야 할지 모호해집니다. 이런 상태에서 콘텐츠만 보강하면 추천 근거가 더 흔들릴 수 있습니다.

| 항목 | Product schema | Merchant feed | 충돌 시 영향 |
|---|---|---|---|
| 가격 | 페이지에 표시된 가격 구조화 | 판매 채널에 전달되는 가격 | 할인/쿠폰 설명 오해 |
| 재고 | 상품 상태 표시 | 구매 가능 여부 | 품절 상품 추천 위험 |
| 리뷰 | 평점/리뷰 수 구조화 | 채널에 따라 제한적 | 신뢰 신호 약화 |
| 배송 | 페이지/정책 문서와 연결 | 배송비/기간 정보 | 구매 전 조건 누락 |

## HaloX 사이트 진단으로 보는 기준

사이트 진단에서는 상품 URL이 검색엔진과 AI crawler에게 읽히는지 확인합니다. 이때 단순 점수보다 URL별 이슈를 봐야 합니다. 핵심 상품 페이지가 canonical 문제, robots 제한, 메타 누락, schema 오류를 갖고 있다면 인용 추적에서 공식 URL이 약하게 잡힐 수 있습니다.

프롬프트 분석과 인용 추적 결과도 함께 봅니다. 특정 조건형 질문에서 경쟁 상품만 citation으로 반복된다면, 그 질문에 필요한 속성이 schema/feed/상세 중 어디에 빠졌는지 확인합니다.

![Schema와 feed 충돌 우선순위 지도](../assets/images/body-figures/halox-geo-11-03-schema-feed-conflict-priority-map-codex-only.png)

*schema와 feed 점검은 오류 찾기가 아니라 구매 질문에서 빠지는 근거를 데이터 층별로 찾는 작업이다.*

## AcmeStore 적용 예시

AcmeStore의 러닝화 상품은 상세 페이지에서 “여성용 경량 러닝화”라고 설명하지만, schema에는 성별/무게 정보가 없고 feed에는 색상 옵션이 일부만 전달됩니다. AI 답변은 “초보 여성 러너용 신발” 질문에서 경쟁 상품을 더 구체적으로 추천합니다.

이때 수정 순서는 명확합니다. 먼저 상세 페이지의 핵심 속성을 구조화하고, Product schema에 가격/재고/브랜드/리뷰 값을 맞춥니다. 그다음 merchant feed의 옵션, 재고, 배송 값을 실제 구매 가능 상태와 맞춥니다. 마지막으로 같은 질문 세트에서 공식 URL citation이 생기는지 확인합니다.

## 정리 양식

```text
상품 URL:
조건형 구매 질문:
상세 페이지 핵심 속성:
Product schema 누락/오류:
merchant feed 누락/오류:
가격/재고/배송 충돌:
수정 담당:
재측정 질문:
```

## 다음 흐름

schema/feed를 맞춘 뒤에는 2주 단위로 위험 상품과 질문을 재측정해야 합니다. 이어서 [커머스 GEO 리스크 2주 점검](https://wikidocs.net/346600)을 봅니다.
