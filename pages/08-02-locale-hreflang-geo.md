## Locale/hreflang과 글로벌 GEO URL 전략

![Locale hreflang 글로벌 GEO](../assets/images/page-heroes/halox-geo-08-02-locale-hreflang-geo-hero.png)

글로벌 GEO에서 URL 구조는 AI와 검색엔진이 “이 페이지가 어느 언어/시장용 답변인가”를 판단하는 기준입니다. 같은 내용이 `/ko/`, `/en/`, `/jp/`에 흩어져 있는데 hreflang, canonical, sitemap이 맞지 않으면 대표 URL이 흔들립니다.

영문 페이지를 만들었는데 AI 답변이 한국어 URL이나 오래된 블로그를 인용한다면 콘텐츠 품질뿐 아니라 locale 신호도 함께 봐야 합니다.

[TOC]

## URL 신호는 언어와 시장을 분리한다

| 항목 | 확인할 것 | 흔한 문제 |
|---|---|---|
| URL 구조 | `/en/`, `/ko/`, 국가/언어 기준 | 언어와 국가가 섞임 |
| hreflang | 상호 참조, x-default | 한쪽 페이지만 선언 |
| canonical | 대표 URL | 영문 페이지가 한국어 canonical을 가리킴 |
| sitemap | 언어별 URL 포함 | 새 locale URL 누락 |
| 내부 링크 | 같은 언어권 링크 | 영문 글에서 한국어 CTA만 연결 |

## HaloX 사이트 진단과 연결하는 법

사이트 진단에서는 URL별 title, description, canonical, robots meta, HTTP 상태를 봅니다. 글로벌 GEO에서는 여기에 hreflang, sitemap, 내부 링크 언어, 페이지 본문 언어 일관성을 추가로 확인합니다.

프롬프트 분석에서는 영어 질문과 한국어 질문을 섞지 않습니다. 같은 제품이라도 “AI search visibility report”와 “AI 검색 리포트”는 별도 기준선으로 측정해야 합니다.

인용 추적에서는 영어 질문에서 어떤 locale URL이 citation 되는지 봅니다. 영문 질문인데 한국어 URL이 반복 인용되면 영문 자산이 약하거나 locale 신호가 불명확할 수 있습니다.

![Locale hreflang canonical 리스크 지도](../assets/images/body-figures/halox-geo-08-02-locale-hreflang-canonical-risk-map-codex-only.png)

*글로벌 URL 전략은 번역 페이지 수가 아니라 대표 locale URL이 안정적으로 인용되는지로 판단한다.*

## AcmeGlobal 적용 예시

AcmeGlobal은 `/en/geo-report`를 만들었지만 canonical이 한국어 원문을 가리킵니다. sitemap에는 영문 URL이 누락되어 있고, 영문 페이지의 CTA는 한국어 docs로 연결됩니다. AI 답변은 영어 질문에서도 한국어 블로그를 인용합니다.

수정은 영문 URL의 canonical과 hreflang을 바로잡고, sitemap에 포함하며, 영문 내부 링크를 영문 docs/guide로 연결하는 것입니다. 이후 같은 영어 질문으로 citation URL이 바뀌는지 확인합니다.

## 점검 양식

```text
시장/언어:
대표 질문:
대표 URL:
hreflang 상태:
canonical 상태:
sitemap 포함 여부:
내부 링크 언어:
현재 citation URL:
수정 티켓:
재측정 질문:
```

## 다음 흐름

URL 신호를 맞춘 뒤에는 시장별로 신뢰받는 외부 출처를 설계해야 합니다. 이어서 [글로벌 source map](https://wikidocs.net/346361)을 봅니다.
