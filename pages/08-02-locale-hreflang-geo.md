## Locale/hreflang과 글로벌 GEO URL 전략

![Locale hreflang 글로벌 GEO](../assets/images/page-heroes/halox-geo-08-02-locale-hreflang-geo-hero.png)

글로벌 GEO에서 URL 구조는 AI와 검색엔진이 “이 페이지가 어느 언어/시장용 답변인가”를 판단하는 기준입니다. 같은 내용이 `/ko/`, `/en/`, `/jp/`에 흩어져 있는데 hreflang, canonical, sitemap이 맞지 않으면 대표 URL이 흔들립니다.

영문 페이지를 만들었는데 AI 답변이 한국어 URL이나 오래된 블로그를 인용한다면 콘텐츠 문장만 고쳐서는 부족합니다. 언어별 대표 URL, canonical, hreflang, sitemap, 내부 링크까지 함께 확인해야 합니다.

[TOC]

## URL 신호는 언어와 시장을 분리한다

| 항목 | 확인할 것 | 흔한 문제 |
|---|---|---|
| URL 구조 | `/en/`, `/ko/`, 국가/언어 기준 | 언어와 국가가 섞임 |
| hreflang | 상호 참조, x-default | 한쪽 페이지만 선언 |
| canonical | 대표 URL | 영문 페이지가 한국어 canonical을 가리킴 |
| sitemap | 언어별 URL 포함 | 새 locale URL 누락 |
| 내부 링크 | 같은 언어권 링크 | 영문 글에서 한국어 CTA만 연결 |

## 대표 URL이 흔들리면 좋은 글도 묻힌다

영문 페이지가 AI 답변에 안정적으로 잡히려면 “이 질문에는 이 URL이 대표 답변이다”라는 신호가 분명해야 합니다. 제목과 본문이 영어여도 canonical이 한국어 원문을 가리키거나, sitemap에 영문 URL이 빠져 있거나, 영문 본문 안의 CTA가 한국어 docs로만 이어지면 대표 URL이 흐려질 수 있습니다.

프롬프트 분석에서도 영어 질문과 한국어 질문을 섞지 않습니다. 같은 제품이라도 `AI search visibility report`와 `AI 검색 리포트`는 별도 기준선으로 측정해야 합니다. 인용 추적에서는 영어 질문에서 어떤 locale URL이 citation 되는지 따로 봅니다.

![Locale hreflang canonical 리스크 지도](../assets/images/body-figures/halox-geo-08-02-locale-hreflang-canonical-risk-map.png)

*글로벌 URL 전략은 번역 페이지 수가 아니라 대표 locale URL이 안정적으로 인용되는지로 판단한다.*

## 가상 기업 AcmeGlobal 예시

AcmeGlobal은 이 책에서 설명을 돕기 위해 만든 가상의 B2B SaaS 기업입니다.

AcmeGlobal은 `/en/geo-report`를 만들었지만 canonical이 한국어 원문을 가리킵니다. sitemap에는 영문 URL이 빠져 있고, 영문 페이지의 CTA는 한국어 docs로 연결됩니다. AI 답변은 영어 질문에서도 한국어 블로그를 인용합니다.

이 경우 수정 순서는 분명합니다. 영문 URL의 canonical을 바로잡고, hreflang 상호 참조를 확인하고, sitemap에 포함합니다. 그다음 영문 내부 링크를 영문 docs/guide로 연결합니다. 수정 후에는 같은 영어 질문으로 citation URL이 바뀌는지 확인합니다.

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
