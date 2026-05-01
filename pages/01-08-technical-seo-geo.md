## 테크니컬 SEO 기본과 GEO 기술 점검

테크니컬 SEO는 검색엔진이 페이지를 발견하고, 읽고, 색인하고, 올바른 URL로 이해하게 만드는 작업입니다. GEO에서도 이 기본은 그대로 중요합니다. AI 검색이 어떤 방식으로 답변 근거를 모으든, 공개 페이지가 발견되지 않거나 본문이 제대로 읽히지 않으면 답변 재료가 되기 어렵습니다.

그래서 테크니컬 SEO는 GEO에서 “개발팀 체크리스트”가 아니라 `AI가 발견하고 읽고 해석할 수 있는 상태`를 만드는 기본 조건입니다.

[TOC]

## 테크니컬 SEO의 기본 축

| 축 | 확인할 것 | GEO에서 중요한 이유 |
|---|---|---|
| 발견 | sitemap, 내부 링크, URL 구조 | AI/검색 크롤러가 중요한 페이지를 찾을 수 있어야 함 |
| 접근 | robots.txt, status code, 로그인/차단 여부 | 공개 답변 근거가 될 페이지는 접근 가능해야 함 |
| 해석 | HTML 본문, heading, schema, canonical | 페이지 주제와 대표 URL이 명확해야 함 |
| 안정성 | 리다이렉트, 사이트 이전, 중복 URL | source/citation이 깨지거나 분산되지 않아야 함 |
| 최신성 | 업데이트 날짜, sitemap 반영, 오래된 정보 | AI 답변에 낡은 정보가 반복되지 않아야 함 |

이 다섯 축은 06장에서 더 깊게 다루는 테크니컬 GEO의 입구입니다.

## sitemap/robots/canonical/schema를 한 번에 보기

| 항목 | 역할 | 흔한 문제 | 먼저 할 일 |
|---|---|---|---|
| sitemap | 중요한 URL 목록을 알려줌 | 핵심 페이지가 빠져 있음 | 핵심 URL 포함 여부 확인 |
| robots.txt | 크롤러 접근 규칙을 알려줌 | 필요한 경로가 차단됨 | 차단 규칙과 실제 URL 비교 |
| canonical | 대표 URL을 지정함 | 중복 페이지가 엉뚱한 URL로 묶임 | 대표 URL과 내부 링크 일치 확인 |
| schema | 본문 정보를 구조화함 | 본문에 없는 정보를 과장 표시 | 본문 정보와 JSON-LD 일치 확인 |
| 내부 링크 | 사이트 안의 관계를 연결함 | 중요한 페이지가 고립됨 | 허브/카테고리에서 연결 |

## GEO 관점의 기술 질문

| SEO 질문 | GEO 확장 질문 |
|---|---|
| 이 URL이 색인되는가? | AI가 이 URL을 답변 근거 후보로 찾을 수 있는가? |
| title/meta가 있는가? | 페이지가 어떤 질문에 답하는지 상단에서 분명한가? |
| schema가 유효한가? | schema가 본문과 같은 내용을 구조화하는가? |
| canonical이 맞는가? | AI가 인용해야 할 대표 URL이 흔들리지 않는가? |
| 내부 링크가 있는가? | 관련 개념과 사례가 연결되어 주제 권위가 보이는가? |

이렇게 바꾸면 기술 점검도 개발 이슈가 아니라 답변 근거 관리가 됩니다.

## 크롤링/색인/랭킹을 GEO 관점으로 보기

테크니컬 SEO를 너무 어렵게 느끼는 이유는 용어가 개발 쪽으로 보이기 때문입니다. 하지만 실무자는 먼저 아래 세 질문만 잡아도 됩니다.

| 개념 | 쉬운 설명 | 확인 예시 | GEO에서의 의미 |
|---|---|---|---|
| 크롤링 | 검색엔진이 URL을 찾고 방문함 | sitemap에 핵심 URL이 있는가, 내부 링크로 갈 수 있는가 | AI가 답변 근거 후보를 발견할 수 있음 |
| 색인 | 검색엔진이 페이지를 저장하고 검색 대상으로 삼음 | noindex/차단/중복 canonical 문제가 없는가 | 공개 답변 재료가 누락되지 않음 |
| 랭킹 | 검색 의도에 맞춰 결과 순서를 정함 | title, 본문, 링크, 권위 신호가 의도와 맞는가 | AI가 후보와 근거를 고를 때 참고할 가능성이 커짐 |

### 기술 점검 예시

| URL | 발견 | 접근 | 해석 | 리스크 | 액션 |
|---|---|---|---|---|---|
| /geo-tools | sitemap 포함, 내부 링크 2개 | 200 OK | title은 좋지만 FAQ schema 없음 | 비교형 질문에서 근거 부족 | 비교표/FAQ/schema 보강 |
| /ai-search-report | sitemap 누락 | 200 OK | canonical 정상 | 핵심 리포트 페이지 발견 약함 | sitemap 추가, 허브 페이지에서 링크 |
| /old-geo-guide | 내부 링크 있음 | 301 이동 | canonical이 옛 URL | citation이 낡은 URL로 갈 수 있음 | 리다이렉트/canonical 정리 |

이 정도 표만 있어도 콘텐츠팀과 개발팀이 같은 언어로 이야기할 수 있습니다. GEO에서 기술 점검의 목적은 완벽한 개발 문서가 아니라 `AI가 참고해야 할 URL을 안정적으로 열어 두는 것`입니다.

## 실무 점검 순서

테크니컬 SEO는 한 번에 모든 것을 보려고 하면 어렵습니다. GEO 입문 단계에서는 핵심 URL 10개만 골라 `발견 → 접근 → 해석 → 안정성 → 최신성` 순서로 봅니다.

1. AI 답변 근거가 되어야 할 핵심 URL 10개를 고릅니다.
2. sitemap에 포함되어 있는지 확인합니다.
3. robots.txt와 robots meta가 접근을 막지 않는지 확인합니다.
4. URL이 200 OK인지, 로그인/스크립트 의존으로 본문이 비어 있지 않은지 봅니다.
5. canonical이 대표 URL을 가리키는지 확인합니다.
6. title, H2, 첫 문단이 같은 주제를 말하는지 봅니다.
7. schema가 본문과 충돌하지 않는지 검증합니다.
8. Google Search Console URL 검사, Rich Results Test, PageSpeed Insights 같은 공식 도구로 확인합니다.

| 점검 단계 | 확인 도구/방법 | 실패 예시 | 수정 방향 |
|---|---|---|---|
| 발견 | sitemap, 내부 링크 | 핵심 리포트 페이지가 sitemap에 없음 | sitemap 추가, 허브 페이지 링크 추가 |
| 접근 | robots.txt, HTTP status | `/reports/`가 robots로 차단 | 차단 규칙 조정 |
| 해석 | title/H2/본문/schema | title은 GEO인데 본문은 일반 SEO | 페이지 주제와 구조 통일 |
| 안정성 | canonical, redirect | 옛 URL이 canonical로 남음 | 대표 URL과 내부 링크 정리 |
| 최신성 | 업데이트 날짜, 변경 이력 | 옛 기능 설명이 인용됨 | 최신 문단과 뉴스룸 링크 보강 |

## 간단한 확인 예시

```text
URL: /geo-tools
sitemap: 포함
robots: 허용
status: 200 OK
canonical: www.example.com/geo-tools
title/H2: GEO 도구 비교와 일치
schema: Article + FAQPage, 본문 FAQ와 일치
리스크: 가격 정보가 오래됨
액션: 가격/기능 업데이트 후 GSC URL 검사 요청
```

이 정도만 기록해도 콘텐츠팀은 어떤 페이지를 고쳐야 하는지, 개발팀은 어떤 기술 이슈를 처리해야 하는지 같은 표를 볼 수 있습니다.

## 기술 이슈를 GEO 지표로 연결하기

| 기술 이슈 | SEO 영향 | GEO 영향 | 우선순위 |
|---|---|---|---|
| noindex가 걸린 핵심 페이지 | 검색결과에 나오지 않음 | 답변 근거 후보에서 빠질 수 있음 | 매우 높음 |
| canonical이 잘못됨 | 대표 URL 신호 분산 | source/citation이 엉뚱한 URL로 잡힘 | 높음 |
| CSR로 본문이 늦게 렌더링됨 | 크롤러가 본문을 약하게 읽을 수 있음 | AI가 요약할 본문이 부족해질 수 있음 | 높음 |
| schema가 본문과 다름 | 리치 결과/신뢰 문제 | 구조화 신호와 본문 신호 충돌 | 중간~높음 |
| 내부 링크가 약함 | 중요 페이지 발견이 약함 | 주제 권위와 맥락 연결이 약함 | 중간 |

## 참고 링크

- Google의 [사이트맵 문서](https://developers.google.com/search/docs/crawling-indexing/sitemaps/overview)는 핵심 URL 발견 상태를 점검할 때 참고합니다.
- Google의 [robots.txt 소개](https://developers.google.com/search/docs/crawling-indexing/robots/intro)는 크롤러 접근 차단 여부를 볼 때 참고합니다.
- Google의 [중복 URL 통합/canonical 문서](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls)는 대표 URL 정리에 필요합니다.
- Google의 [구조화 데이터 소개](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data)는 schema와 본문 일치 여부를 검토할 때 참고합니다.

## 실습 워크시트

| 입력 항목 | 작성 기준 |
|---|---|
| 핵심 URL | AI 답변 근거가 되어야 할 페이지 |
| 발견 상태 | sitemap 포함/내부 링크 유무 |
| 접근 상태 | robots/status code/로그인 차단 여부 |
| 해석 상태 | title/H2/본문/schema/canonical 일치 여부 |
| 인용 리스크 | URL 변경, 중복, 낡은 정보, 차단 가능성 |
| 수정 담당 | 콘텐츠/개발/SEO/브랜드 중 담당 |

```text
핵심 URL / 발견 상태 / 접근 상태 / 해석 상태 / 인용 리스크 / 수정 담당
```

## 완료 기준

- 핵심 URL이 sitemap과 내부 링크에서 발견됩니다.
- robots/canonical/schema가 서로 충돌하지 않습니다.
- 본문과 구조화 데이터가 같은 내용을 말합니다.
- 더 깊은 점검은 [06장 테크니컬 GEO](https://wikidocs.net/346346)로 넘길 수 있습니다.

다음은 [권위 신호와 엔티티를 GEO로 확장하기](https://wikidocs.net/346928)입니다.
