## SEO 기본기와 GEO 확장 전략

SEO는 검색엔진에서 순위를 올리는 기술만을 뜻하지 않습니다. 좋은 SEO 운영은 사람들이 어떤 말로 문제를 찾는지 발견하고, 그 문제에 답할 콘텐츠를 설계하고, 검색엔진과 AI가 읽을 수 있는 구조로 정리한 뒤, 신뢰 신호와 측정 데이터로 계속 개선하는 일입니다.

GEO도 여기서 출발합니다. AI 검색은 사용자의 질문에 바로 답을 만들지만, 그 답변의 재료는 결국 웹에 공개된 콘텐츠, 출처, 브랜드 설명, 기술 구조, 외부 언급에서 나옵니다. SEO의 기본기가 약하면 AI 답변에 들어갈 재료도 약해집니다. 그래서 이 장은 `SEO와 GEO의 차이`를 설명하는 장이 아니라, SEO 실무 흐름을 GEO 실행의 기초 체력으로 바꾸는 장입니다.

[TOC]

## 이 장에서 다루는 전체 흐름

1장은 하나의 흐름으로 읽어야 합니다. 키워드를 모으고, SERP를 분석하고, 검색 의도를 해석하고, 콘텐츠 구조를 잡고, 온페이지 요소를 정리하고, 내부 링크로 문맥을 연결하고, 기술 SEO로 읽힐 조건을 만들고, 권위와 엔티티 신호를 보강한 뒤, 측정 데이터로 다시 개선합니다.

```text
키워드 리서치 → SERP 분석 → 검색 의도 → 콘텐츠 구조 → 온페이지 SEO → 내부 링크 → 테크니컬 SEO → 권위/백링크/엔티티 → 측정/개선 → GEO 질문셋 확장
```

이 순서가 중요한 이유는 각 단계가 다음 단계의 입력값이 되기 때문입니다. 키워드 리서치를 제대로 하지 않으면 SERP 분석의 기준이 흔들립니다. SERP 분석 없이 검색 의도를 판단하면 콘텐츠 구조가 추측이 됩니다. 콘텐츠 구조가 약하면 온페이지 SEO는 title과 meta만 고치는 작업으로 축소됩니다. 내부 링크와 기술 SEO가 약하면 좋은 글도 검색엔진과 AI가 충분히 발견하지 못합니다. 권위와 엔티티 신호가 약하면 AI가 브랜드를 어떤 카테고리의 답으로 이해해야 하는지 흔들립니다. 측정이 없으면 무엇을 고쳐야 하는지 알 수 없습니다.

## SEO 실무는 팀 작업이다

SEO를 한 사람이 전부 처리하는 업무로 보면 실행이 얕아집니다. 실제 운영에서는 여러 팀이 같은 흐름을 공유해야 합니다.

콘텐츠팀은 사용자가 이해할 수 있는 답변 구조를 만듭니다. SEO 담당자는 키워드, SERP, 검색 의도, 내부 링크, 측정 기준을 연결합니다. 개발팀은 크롤링, 색인, 렌더링, schema, 속도, canonical 같은 기술 조건을 처리합니다. 브랜드팀과 PR팀은 외부에서 브랜드가 어떤 문장으로 설명되는지 관리합니다. 데이터팀이나 마케팅 운영 담당자는 GSC, GA4, 네이버 서치어드바이저, AI 답변 측정 결과를 리포트로 묶습니다.

1장의 목표는 이 팀들이 같은 언어로 이야기할 수 있게 만드는 것입니다. `순위가 낮다`, `AI 답변에 안 나온다`, `전환이 안 된다` 같은 증상을 각각 따로 보지 않고, 어느 단계에서 병목이 생겼는지 찾는 방식으로 바꿉니다.

## SEO에서 GEO로 넘어갈 때 바뀌는 질문

기존 SEO에서는 자주 이런 질문을 합니다.

- 이 키워드에서 우리 페이지가 몇 위인가?
- 이 페이지의 CTR은 왜 낮은가?
- 어떤 검색어에서 유입이 생기는가?
- 어떤 페이지가 전환에 기여하는가?

GEO에서는 이 질문이 조금 바뀝니다.

- 이 질문에서 우리 브랜드가 AI 답변에 언급되는가?
- AI는 어떤 출처를 근거로 답하는가?
- 우리 페이지가 source나 citation으로 잡히는가?
- 경쟁사는 어떤 이유로 추천되고 우리는 왜 빠지는가?
- 검색 유입과 AI 답변 노출을 함께 보면 다음 액션은 무엇인가?

하지만 완전히 다른 일이 아닙니다. SEO에서 쌓은 query, page, intent, content, link, technical, authority, measurement 데이터가 GEO 질문셋과 답변 근거 전략의 입력값이 됩니다.

## 1장에서 남겨야 할 산출물

이 장을 읽고 나면 단순히 개념을 이해하는 데서 끝나면 안 됩니다. 아래 산출물이 남아야 합니다.

| 단계 | 산출물 | 다음 단계에서 쓰이는 곳 |
|---|---|---|
| 키워드 리서치 | 핵심 키워드와 롱테일 질문 후보 | SERP 분석/AI 질문셋 |
| SERP 분석 | 상위 결과 유형, 반복 구조, 콘텐츠 갭 | 검색 의도/콘텐츠 구조 |
| 검색 의도 | 정보형/비교형/추천형/검증형/실행형 분류 | 콘텐츠 형식 결정 |
| 콘텐츠 구조 | Answer-first 목차, 표/FAQ/사례/CTA 설계 | 온페이지 SEO |
| 온페이지 SEO | title/meta/H2/첫 문단/schema 초안 | 검색결과와 AI 답변 재료 |
| 내부 링크 | 허브/클러스터/앵커 텍스트 맵 | 주제 권위와 탐색 흐름 |
| 테크니컬 SEO | 발견/접근/해석/안정성 점검표 | source/citation 후보 안정화 |
| 권위/엔티티 | 외부 출처 후보, 브랜드 설명 문장 | AI 답변의 신뢰 신호 |
| 측정/개선 | GSC/GA4/네이버/AI 답변 리포트 | 다음 30일 실행 계획 |

## AcmeGEO 예시로 보는 전체 흐름

이 장 전체에서는 가상의 B2B SaaS 브랜드 `AcmeGEO`를 예시로 씁니다. AcmeGEO는 AI 검색에서 브랜드가 어떻게 언급되는지 측정하는 도구입니다. 팀은 `GEO 도구`, `AI 검색 모니터링`, `ChatGPT 브랜드 노출`, `GEO 리포트` 같은 키워드에서 검색 노출과 AI 답변 노출을 함께 늘리고 싶어 합니다.

처음에는 `GEO 도구`라는 키워드만 보입니다. 하지만 키워드 리서치를 해보면 사용자는 단순히 도구 이름을 찾는 것이 아닙니다. 어떤 팀은 GEO가 무엇인지 알고 싶어 하고, 어떤 팀은 기존 SEO 도구와 무엇이 다른지 비교하고 싶어 하고, 어떤 팀은 대행사 리포트를 검증하고 싶어 합니다. SERP를 보면 상위 글 대부분이 개념 설명이나 도구 목록에 머물고, 실제로 어떤 지표를 봐야 하는지 설명하는 글은 부족합니다.

이때 AcmeGEO가 해야 할 일은 `GEO 도구` 키워드를 반복하는 글을 쓰는 것이 아닙니다. 검색 의도별로 답변 구조를 나누고, 비교 기준과 측정 절차를 제시하고, 제품 소개 페이지와 리포트 예시 페이지를 내부 링크로 연결하고, 기술적으로 색인 가능하게 만들고, 외부 디렉터리와 뉴스룸에서 같은 카테고리 설명이 반복되게 해야 합니다. 이후 GSC와 GA4, AI 답변 측정 결과를 보며 어떤 질문에서 언급이 생기고 어떤 질문에서 빠지는지 다시 확인합니다.

## SEO 실무 키워드 커버리지 지도

1장은 GEO를 설명하기 위한 SEO 요약이 아니라, SEO 실무자가 실제로 쓰는 개념을 GEO 흐름에 연결하는 장입니다. 그래서 각 페이지는 아래 SEO 키워드 묶음을 맡습니다.

| 실무 영역 | 핵심 SEO 키워드 | 1장에서 다루는 위치 |
|---|---|---|
| 키워드 리서치 | seed keyword, search volume, keyword difficulty, long-tail, branded/non-branded, keyword clustering, cannibalization | 01-01 |
| SERP 분석 | page type, SERP feature, featured snippet, People Also Ask, freshness, content depth, Naver SERP | 01-02 |
| 검색 의도 | informational, navigational, commercial, transactional, TOFU/MOFU/BOFU, mixed intent, intent mismatch | 01-03 |
| 콘텐츠 구조 | content brief, Answer-first, topical authority, H2/H3, FAQ, CTA, content refresh | 01-04 |
| 온페이지 SEO | title, meta description, URL slug, H1/H2, image alt, schema, CTR 개선 | 01-05 |
| 내부 링크 | hub, cluster, anchor text, orphan page, topic cluster, contextual link | 01-06 |
| 테크니컬 SEO | crawl, render, index, robots, noindex, canonical, status code, Core Web Vitals, structured data validation | 01-07 |
| 권위/엔티티 | backlink, referring domain, topical relevance, anchor text profile, E-E-A-T, entity, brand mention, sameAs | 01-08 |
| 측정/개선 | GSC, GA4, Naver Search Advisor, impressions, CTR, average position, key event, KPI, content decay | 01-09 |
| 통합 운영 | SEO brief, technical ticket, source map, monthly report, 30-day action plan | 01-10 |

이 키워드들은 단순 용어 목록이 아닙니다. 각 개념이 실제 페이지 작성, 기술 점검, 외부 출처 설계, 월간 리포트에서 어떻게 쓰이는지 연결해서 봐야 합니다.

## 읽는 순서

1. [01-01. 키워드 리서치](https://wikidocs.net/346313)에서 시장 언어를 모으는 법을 배웁니다.
2. [01-02. SERP 분석](https://wikidocs.net/346314)에서 검색결과를 의도 지도로 읽습니다.
3. [01-03. 검색 의도](https://wikidocs.net/346339)에서 키워드 뒤의 목적을 해석합니다.
4. [01-04. 콘텐츠 구조](https://wikidocs.net/346340)에서 검색 의도를 답변 구조로 바꿉니다.
5. [01-05. 온페이지 SEO](https://wikidocs.net/346341)에서 title, meta, heading, 첫 문단을 정리합니다.
6. [01-06. 내부 링크](https://wikidocs.net/346925)에서 허브/클러스터와 앵커 맵을 만듭니다.
7. [01-07. 테크니컬 SEO](https://wikidocs.net/346926)에서 발견/접근/해석 조건을 점검합니다.
8. [01-08. 권위/백링크/엔티티](https://wikidocs.net/346927)에서 외부 신뢰 신호를 설계합니다.
9. [01-09. 측정/개선](https://wikidocs.net/346928)에서 GSC, GA4, 네이버, AI 답변 지표를 묶습니다.
10. [01-10. SEO에서 GEO로 확장하는 통합 실습](https://wikidocs.net/346933)에서 하나의 키워드로 전체 실행안을 만듭니다.
