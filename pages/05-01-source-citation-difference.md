## 답변 근거(source)와 화면 인용(citation) 차이

![답변 근거와 화면 인용의 차이](../assets/images/page-heroes/halox-geo-05-01-source-citation-difference-hero.png)

답변 근거(source)와 화면 인용(citation)은 같은 말이 아닙니다. source는 AI가 답변을 만들 때 참고한 근거에 가깝고, citation은 사용자가 화면에서 볼 수 있는 인용 링크입니다.

GEO에서 이 둘을 나눠야 하는 이유는 액션이 다르기 때문입니다. source가 약하면 브랜드와 주제에 대한 근거 자산을 늘려야 하고, citation이 약하면 URL 단위의 답변 구조와 기술 조건을 점검해야 합니다.

[TOC]

## 04장과 연결해서 본다

04장에서 페이지를 Answer-first로 고쳤다면, 05장에서는 그 페이지가 답변 근거와 화면 인용 후보가 될 수 있는지 봅니다. 좋은 문장만으로는 부족합니다. AI가 신뢰할 만한 출처로 볼 수 있는 공식성, 반복성, 외부 합의 신호가 함께 필요합니다.

| 구분 | 보는 질문 | 주요 액션 |
|---|---|---|
| source | 답변의 근거로 쓰일 만한가 | 공식 설명, 사례, 외부 출처 보강 |
| citation | 화면에 링크로 보일 만한가 | URL 구조, 첫 답변, 제목, schema 점검 |
| mention | 브랜드가 답변에 등장하는가 | 카테고리/비교 문맥 보강 |

## 플랫폼마다 다르게 보인다

ChatGPT에서는 citation이 항상 보이지 않을 수 있습니다. Perplexity는 답변과 인용 URL의 연결을 비교적 확인하기 좋습니다. Google AI Overviews는 기존 검색결과, AI 요약, 출처 표시가 함께 움직입니다.

그래서 “인용이 없다”는 말만으로 판단하지 않습니다. 어떤 플랫폼에서, 어떤 질문군에서, 어떤 URL이, 어떤 문장의 근거로 쓰였는지를 함께 기록합니다.

![source와 citation 이중 레이어](../assets/images/body-figures/halox-geo-05-01-source-citation-dual-layer-codex-only.png)

*source는 답변의 근거 층이고, citation은 사용자가 확인하는 화면 링크 층이다.*

## 실제 질문에서 나눠 읽기

`AI 검색 브랜드 가시성 분석 도구 추천`이라는 질문에서 AcmeGEO가 언급됐지만 공식 URL은 인용되지 않았다고 가정해 보겠습니다. 이 경우 mention은 있지만 citation은 약합니다. 답변 문장에 “브랜드 언급률과 citation을 분리해 보는 도구”라고 설명됐다면 source 신호는 일부 있는 상태일 수 있습니다.

다음 액션은 단순히 “더 많이 노출되기”가 아닙니다.

- 공식 페이지에 mention/source/citation 구분을 명확히 쓴다.
- 리포트 예시 URL을 만든다.
- 외부 가이드나 사례에서 같은 기준을 반복한다.
- 같은 질문군으로 citation 변화를 다시 본다.

## 먼저 볼 체크포인트

1. 브랜드가 어떤 질문에서 언급되는가
2. 답변 근거로 보이는 URL이나 문맥이 있는가
3. 화면에 citation으로 보이는 URL은 무엇인가
4. 경쟁 URL은 어떤 문장의 근거로 쓰이는가
5. 우리 URL이 빠진 이유가 콘텐츠/출처/기술 중 어디에 가까운가

## 정리 양식

```text
질문:
플랫폼:
브랜드 mention:
source로 보이는 근거:
citation URL:
경쟁 citation URL:
빠진 이유 추정:
다음 액션:
```

## 다음 흐름

source/citation의 차이를 잡았다면 [엔티티와 브랜드 합의 신호](https://wikidocs.net/346351)에서 여러 채널의 브랜드 설명이 같은 방향으로 쌓이는지 봅니다.
