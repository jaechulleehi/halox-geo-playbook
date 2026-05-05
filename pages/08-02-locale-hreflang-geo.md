## Locale/hreflang과 글로벌 GEO URL 전략

![Locale hreflang GEO 점검](../assets/images/page-heroes/halox-geo-08-02-locale-hreflang-geo-hero.png)

Locale과 hreflang은 다국어 사이트에서 언어/지역별 대표 URL을 알려주는 신호입니다. GEO에서는 AI가 한국어 페이지, 영어 페이지, 지역별 페이지를 혼동하지 않도록 돕는 역할을 합니다.

hreflang이 있어도 canonical이 엇갈리거나 sitemap이 섞이면 source/citation 후보가 흔들릴 수 있습니다. 글로벌 GEO에서는 콘텐츠 번역과 기술 신호를 함께 봐야 합니다.

[TOC]

## 먼저 볼 기준

| 기준 | 읽는 법 |
|---|---|
| URL | 언어/지역별 URL 구조가 일관적인지 본다 |
| canonical | 각 언어 페이지가 올바른 대표 URL을 가리키는지 본다 |
| hreflang | 상호 참조와 sitemap 반영을 확인한다 |

## 실행 흐름

1. 대표 질문을 정한다.
2. 현재 AI 답변에서 mention/source/citation을 나눠 본다.
3. 경쟁 브랜드나 반복 URL이 어떤 이유로 등장하는지 확인한다.
4. 우리 공식 페이지, 외부 출처, 기술 조건 중 먼저 고칠 곳을 고른다.
5. 같은 질문군으로 30일 뒤 다시 본다.

![언어/지역 URL과 canonical 정렬](../assets/images/body-figures/halox-geo-08-02-locale-hreflang-canonical-risk-map-codex-only.png)

*언어/지역 URL과 canonical 정렬*

## locale 예시

AcmeGEO의 `/ko/` 페이지와 `/en/` 페이지가 서로 다른 카테고리 설명을 쓰고, canonical이 한쪽으로만 잡히면 영어권 답변에서 한국어 URL이 citation 후보로 나올 수 있습니다. 언어별 대표 URL과 기준 문장을 함께 정리합니다.

## 정리 양식

```text
언어/지역:
URL 구조:
canonical:
hreflang 쌍:
sitemap:
재점검 질문:
```

## 다음 흐름

글로벌 외부 근거는 [글로벌 답변 근거 맵](https://wikidocs.net/346361)에서 설계합니다.
