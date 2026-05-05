## Schema와 내부 링크로 AI 이해도 높이기

![Schema와 내부 링크 구조](../assets/images/page-heroes/halox-geo-06-05-schema-internal-link-structure-hero.png)

Schema와 내부 링크는 페이지의 의미를 정리하는 보조 장치입니다. schema는 페이지에 담긴 조직/상품/FAQ/글 정보를 구조화하고, 내부 링크는 관련 페이지 사이의 관계를 보여줍니다.

둘 다 본문을 대신하지 않습니다. 화면에 없는 정보를 schema에만 넣거나, 실제 연결이 없는 페이지를 억지로 묶으면 오히려 해석이 흐려집니다.

[TOC]

## schema는 본문 정보의 구조화다

가장 흔한 방식은 JSON-LD입니다. 예시는 간단히 보면 아래와 같습니다.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "AcmeGEO",
  "url": "https://example.com",
  "description": "AI search visibility analysis platform"
}
</script>
```

이 정보는 본문과 충돌하면 안 됩니다. 본문에서는 다른 카테고리로 설명하면서 schema만 다르게 쓰면 합의 신호가 약해집니다.

## 내부 링크는 의미 관계를 만든다

GEO에서 내부 링크는 단순 이동 경로가 아닙니다. “이 질문의 답은 이 페이지에서 시작하고, 근거는 이 페이지에서 확인한다”는 관계를 만듭니다.

| 허브 페이지 | 연결할 페이지 |
|---|---|
| GEO 개념 글 | SEO/GEO 차이, Fan-out, source/citation |
| 리포트 예시 | mention/source/citation, 30일 액션 플랜 |
| 제품 페이지 | 기능 설명, 비교 글, 사례, 가격/도입 안내 |
| 뉴스룸 | 보도자료, 인터뷰, 사례, 회사 프로필 |

![Schema와 내부 링크 의미 구조](../assets/images/body-figures/halox-geo-06-05-schema-internal-link-semantic-mesh-codex-only.png)

*Schema는 정보를 구조화하고, 내부 링크는 페이지 사이의 의미 관계를 만든다.*

## 붙이기 전에 맞출 것

1. 페이지 제목과 첫 문단이 같은 주제를 말하는가
2. schema 타입이 페이지 목적과 맞는가
3. FAQ schema는 화면의 FAQ와 같은가
4. Product/SoftwareApplication 정보가 실제 제품 설명과 맞는가
5. 내부 링크 앵커가 연결 페이지의 주제와 맞는가

## 정리 양식

```text
점검 URL:
페이지 목적:
schema 후보 타입:
본문과 충돌하는 필드:
연결할 내부 링크:
앵커 문구:
검증 도구 결과:
```

## 다음 흐름

schema를 실제 타입별로 나눠 보려면 [Schema 타입별 실전 점검표](https://wikidocs.net/346851)를 읽습니다. 공식 도구 검증은 [Google 공식 도구로 SEO/GEO 기술 상태 점검하기](https://wikidocs.net/346842)에서 다룹니다.
