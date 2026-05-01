## SEO 성과 측정: Google Search Console, GA4, 네이버 웹마스터 도구

SEO와 GEO를 함께 운영하려면 측정 기준을 먼저 정해야 합니다. 기존 SEO에서는 Google Search Console, GA4, 네이버 웹마스터 도구로 검색 노출, 클릭, 유입, 전환, 색인 상태를 확인합니다. GEO에서는 여기에 AI 답변의 mention/source/citation, 질문셋별 답변 변화, 경쟁사 비교를 붙여 봅니다.

이 페이지의 목적은 도구를 많이 나열하는 것이 아닙니다. `검색에서 사람들이 어떻게 발견하고 들어오는가`와 `AI 답변에서 브랜드가 어떻게 설명되는가`를 같은 질문셋으로 연결하는 것입니다.

[TOC]

## SEO 측정과 GEO 측정은 무엇이 다른가

| 구분 | SEO 측정 | GEO 측정 | 함께 봐야 하는 이유 |
|---|---|---|---|
| 노출 | 검색결과에 페이지가 몇 번 보였는가 | AI 답변에 브랜드/페이지가 언급됐는가 | 검색 수요와 AI 답변 노출의 차이를 봄 |
| 클릭 | 사용자가 검색결과에서 클릭했는가 | AI 답변에서 클릭 가능한 citation이 잡혔는가 | 답변 안 노출이 실제 방문으로 이어지는지 확인 |
| 쿼리 | 어떤 검색어에서 노출/클릭됐는가 | 어떤 질문에서 mention/source/citation이 생겼는가 | SEO 키워드를 AI 질문셋으로 확장 |
| 페이지 | 어떤 URL이 유입을 만들었는가 | 어떤 URL이 답변 근거/source로 쓰였는가 | 콘텐츠 보강 우선순위 결정 |
| 전환 | 유입 후 문의/가입/구매가 있었는가 | AI 답변 이후 방문/문의 흐름이 생겼는가 | 리포트를 실행 액션으로 연결 |
| 기술 상태 | 색인, sitemap, robots, canonical 문제 | AI가 참고할 URL이 발견/해석 가능한가 | 06장 기술 점검과 연결 |

SEO 지표는 `검색 유입의 현실`을 보여주고, GEO 지표는 `AI 답변 안에서의 브랜드 위치`를 보여줍니다. 둘 중 하나만 보면 실행 우선순위가 흔들립니다.

## Google Search Console에서 먼저 볼 것

Google Search Console은 SEO/GEO 연결에서 가장 중요한 출발점입니다. 실제 검색어, 노출, 클릭, 평균 순위, 페이지 성과, 색인 상태를 확인할 수 있기 때문입니다.

| 메뉴/지표 | 확인할 것 | GEO로 연결하는 법 |
|---|---|---|
| 검색 결과 성과 | query, page, impressions, clicks, CTR, average position | 노출은 있는데 클릭이 낮은 쿼리를 AI 질문 후보로 전환 |
| 페이지별 성과 | 어떤 URL이 어떤 query에서 보이는가 | source/citation 후보 URL을 고름 |
| 검색어 변화 | 새로 떠오르는 query, 하락한 query | 질문셋 추가/콘텐츠 리라이트 우선순위 결정 |
| 색인 생성 | 색인됨/제외됨/크롤링됨 상태 | 답변 근거가 될 URL이 검색 대상인지 확인 |
| sitemap | 제출 URL과 발견 URL | 핵심 페이지 발견 가능성 확인 |
| 페이지 경험/코어 웹 바이탈 | 모바일/속도/경험 문제 | 기술 SEO 리스크와 개발 액션 연결 |

### GSC 실무 워크플로우

1. 최근 3개월의 query를 export합니다.
2. impressions가 높고 CTR이 낮은 쿼리를 표시합니다.
3. 평균 순위가 5~20위인 쿼리를 따로 봅니다.
4. 해당 쿼리의 landing page를 확인합니다.
5. 쿼리를 정보형/비교형/추천형/실행형으로 분류합니다.
6. 각 쿼리를 AI 질문으로 바꿉니다.
7. 같은 질문으로 ChatGPT/Perplexity/Google AI 기능에서 mention/source/citation을 기록합니다.

이렇게 하면 Search Console은 단순 SEO 리포트가 아니라 GEO 질문셋을 만드는 데이터 소스가 됩니다.

## 네이버 웹마스터 도구에서 볼 것

한국 시장에서는 Google만 보면 부족합니다. 네이버 검색 유입, 네이버 플레이스, 브랜드명 검색, 블로그/카페/지식iN/뉴스 노출이 함께 움직이기 때문입니다. 네이버 웹마스터 도구는 사이트 수집, 색인, 콘텐츠 구조, 검색 노출 상태를 확인하는 기본 도구로 봐야 합니다.

| 확인 항목 | 보는 이유 | GEO/AI 검색 연결 |
|---|---|---|
| 사이트 수집 상태 | 네이버가 핵심 페이지를 가져가는지 확인 | 한국어 브랜드/카테고리 설명의 기본 노출 확인 |
| 색인 현황 | 검색 대상 페이지가 누락되지 않았는지 확인 | AI 답변이 참고할 수 있는 공개 정보 기반 점검 |
| 검색 유입 쿼리 | 네이버 사용자가 실제로 쓰는 표현 확인 | 한국어 AI 질문셋의 표현을 현실화 |
| 사이트맵/robots | 발견/차단 문제 확인 | 01-08/06장 기술 점검과 연결 |
| 구조화/콘텐츠 품질 | 제목, 설명, 본문 구조 확인 | Answer-first 구조와 중복/낡은 정보 점검 |

네이버에서는 특히 로컬/병원/오프라인 매장/커머스/브랜드명 검색의 의미가 큽니다. 그래서 12장의 로컬 SEO/GEO와도 함께 봐야 합니다.

## GA4에서 볼 것

GA4는 검색에서 들어온 사용자가 실제로 무엇을 했는지 봅니다. Search Console이 `검색 전/검색결과`를 보여준다면, GA4는 `유입 후 행동`을 보여줍니다.

| GA4 지표 | 확인할 것 | 실행 판단 |
|---|---|---|
| traffic acquisition | organic search, referral, direct 유입 변화 | SEO/GEO 작업 후 유입 채널 변화 확인 |
| landing page | 어떤 페이지로 들어오는가 | 리라이트/내부 링크/CTA 우선순위 결정 |
| engagement rate | 들어온 뒤 읽고 움직였는가 | 첫 문단, 표, CTA, 페이지 구조 개선 |
| key events/conversions | 문의, 가입, 다운로드, 예약 등 | 검색 유입이 사업 성과로 이어지는지 확인 |
| path exploration | 다음에 어디로 이동하는가 | 내부 링크와 정보 흐름 보강 |
| source/medium | Google, Naver, Perplexity, referral 등 | AI citation/referral 유입 탐지 후보 확인 |

GEO 작업은 “AI 답변에 나왔다”에서 끝나면 안 됩니다. 답변 노출 이후 실제 사이트 방문, 리포트 조회, 문의, 예약, 가입으로 이어지는지를 GA4에서 확인해야 합니다.

## SEO/GEO 통합 리포트 구조

월간 리포트는 SEO 지표와 GEO 지표를 따로 붙이는 방식보다, 같은 질문셋을 기준으로 묶는 편이 좋습니다.

| 리포트 섹션 | 포함할 지표 | 해석 질문 |
|---|---|---|
| 1. 검색 수요 | GSC query, impressions, clicks, CTR, position | 어떤 문제에서 검색 수요가 있는가? |
| 2. 유입 페이지 | GSC page, GA4 landing page, engagement | 어떤 URL이 유입과 행동을 만드는가? |
| 3. AI 답변 노출 | mention, source, citation, competitor mention | 같은 질문에서 AI 답변 안 위치는 어떤가? |
| 4. 기술 상태 | 색인, sitemap, robots, canonical, schema | 핵심 URL이 발견/해석 가능한가? |
| 5. 전환 | GA4 key events, 문의/가입/예약 | 검색/AI 노출이 실제 성과로 이어지는가? |
| 6. 다음 액션 | 리라이트, source 보강, 기술 수정, 질문셋 추가 | 다음 30일에 무엇을 고칠 것인가? |

이 구조를 쓰면 SEO 리포트와 GEO 리포트가 분리되지 않습니다. 하나의 질문셋에 대해 `검색 수요 → 페이지 성과 → AI 답변 위치 → 전환 → 다음 액션`을 한 번에 봅니다.

## AcmeGEO 월간 측정 예시

| 질문/키워드 | GSC 신호 | GA4 신호 | AI 답변 신호 | 다음 액션 |
|---|---|---|---|---|
| GEO 도구 | 노출 높음, CTR 낮음, 평균 9위 | landing page 체류 짧음 | 경쟁사는 언급, AcmeGEO 미언급 | title/첫 문단/비교표 리라이트 |
| AI 검색 모니터링 | 노출 증가, 클릭 보통 | 리포트 페이지 전환 있음 | source는 잡히나 citation 약함 | 리포트 예시와 FAQ 보강 |
| GEO 대행사 선택 기준 | 검색 노출 낮음 | 유입 거의 없음 | AI 답변이 일반론 중심 | 제안서 검증 체크리스트 신규 작성 |
| ChatGPT 브랜드 노출 | Search Console query 증가 | 문의 전환 일부 있음 | mention은 있으나 설명 부정확 | 브랜드 정의/엔티티 문장 정리 |

이 예시에서 우선순위는 단순히 검색량이 큰 키워드가 아닙니다. `GSC에서 수요가 보이고, GA4에서 행동이 있으며, AI 답변에서 빠지거나 부정확한 질문`이 먼저입니다.

## 실습 워크시트

| 입력 항목 | 작성 기준 |
|---|---|
| 핵심 query | GSC/네이버 웹마스터 도구에서 확인한 검색어 |
| 대상 page | 노출/클릭/유입을 만드는 URL |
| SEO 지표 | impressions, clicks, CTR, position, 색인 상태 |
| GA4 지표 | landing page, engagement, key event, conversion |
| AI 질문 | query를 바꾼 측정용 프롬프트 |
| GEO 지표 | mention, source, citation, 경쟁사 언급 |
| 다음 액션 | 리라이트, 기술 수정, source 보강, 질문셋 추가 |

```text
query / page / SEO 지표 / GA4 지표 / AI 질문 / GEO 지표 / 다음 액션
```

## 완료 기준

- Google Search Console에서 핵심 query/page를 뽑았습니다.
- 네이버 웹마스터 도구에서 한국어 검색 유입과 수집/색인 상태를 확인했습니다.
- GA4에서 유입 후 행동과 전환 지표를 확인했습니다.
- SEO query를 AI 질문셋으로 바꾸고 mention/source/citation을 함께 기록했습니다.
- 다음 30일 액션이 콘텐츠/기술/source 보강 중 어디에 속하는지 정리했습니다.

다음은 [02장 AI 검색 모니터링](https://wikidocs.net/346342)에서 이 질문셋을 실제 AI 답변 기준선으로 측정합니다.
