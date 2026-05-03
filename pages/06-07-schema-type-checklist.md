## Schema 타입별 실전 점검표: Organization/Person/FAQ/Product

![Schema 타입별 실전 점검표](../assets/images/page-heroes/halox-geo-06-07-schema-type-checklist-hero.png)

Schema 타입은 페이지의 목적에 맞춰 고릅니다. Organization은 회사/브랜드, Person은 인물, FAQPage는 실제 FAQ, Product 또는 SoftwareApplication은 제품/소프트웨어 설명에 맞습니다.

중요한 원칙은 하나입니다. 화면 본문에 없는 정보를 schema에만 넣지 않습니다. 구조화 데이터는 본문을 보강하는 장치이지 본문을 대체하는 장치가 아닙니다.

[TOC]

## 타입별 역할

| 타입 | 잘 맞는 페이지 |
|---|---|
| Organization | 회사 소개, 브랜드 프로필, 공식 사이트 기준 정보 |
| Person/ProfilePage | 대표자, 저자, 전문가 프로필 |
| FAQPage | 화면에 실제 FAQ가 있는 설명/가이드 페이지 |
| Product/SoftwareApplication | 제품, SaaS, 기능, 가격, 리뷰 정보가 있는 페이지 |

## FAQPage 예시

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [{
    "@type": "Question",
    "name": "GEO 리포트에서 source와 citation은 무엇이 다른가요?",
    "acceptedAnswer": {
      "@type": "Answer",
      "text": "source는 답변 근거이고, citation은 사용자 화면에 보이는 인용 링크입니다."
    }
  }]
}
</script>
```

이 FAQ는 페이지 화면에도 보여야 합니다. schema만 있고 본문에는 없으면 신뢰 신호가 약해질 수 있습니다.

## Product/SoftwareApplication에서 볼 것

제품 schema를 넣을 때는 실제 제품 설명과 맞아야 합니다. 이름, 설명, URL, 카테고리, 가격 정보, 리뷰 정보가 과장되거나 오래되면 안 됩니다.

| 필드 | 확인 기준 |
|---|---|
| name | 공식 제품명과 일치 |
| description | 첫 문단의 제품 설명과 충돌하지 않음 |
| url | canonical 대표 URL과 일치 |
| applicationCategory | 실제 제품 카테고리와 일치 |

![Schema 타입 선택과 fan-out 연결](../assets/images/body-figures/halox-geo-06-07-schema-type-selector-codex-only.png)

*Schema 타입은 페이지 목적과 fan-out 노드에 맞춰 고른다.*

## 선택 순서

1. 페이지가 회사/인물/FAQ/제품 중 무엇을 설명하는지 정한다.
2. 본문에 해당 정보가 실제로 있는지 확인한다.
3. schema 필드와 본문 문장을 맞춘다.
4. Rich Results Test로 오류를 확인한다.
5. 같은 질문군에서 source/citation 변화를 재측정한다.

## 정리 양식

```text
URL:
페이지 목적:
선택 schema 타입:
본문에 보이는 필드:
누락/충돌 필드:
검증 도구 결과:
수정 액션:
```

## 다음 흐름

schema 타입을 고른 뒤에는 [메타 정보 실전 점검](https://wikidocs.net/346855)에서 title, meta description, canonical, robots meta를 함께 봅니다.
