# EXPANSION_AUDIT_CURRENT

## 목적

이 문서는 현재 GEO WikiDocs 책을 1장부터 다시 훑어 보고, HaloX 블로그/글로서리/Obsidian 스터디 자산을 기준으로 어떤 장을 더 확장해야 하는지 판단하기 위한 리뷰입니다.

## 결론

현재 구조는 기본 흐름은 좋습니다. `입문 → 질문 시장 → 측정 → Fan-out → 콘텐츠 구조 → 출처/엔티티 → 기술 구조 → 산업별 적용 → 글로벌 → 도구/리포트 → 4주 실행`의 학습 여정은 유지하는 것이 맞습니다.

다만 지금 책은 아직 “GEO 개론 + 실습 골격”에 가깝습니다. HaloX가 이미 가진 블로그 28개, 글로서리 40개, GEO 스터디 마스터 인덱스, 커머스/AIO/AI 구매 에이전트 노트를 반영하면 장 단위로 더 깊어질 수 있습니다.

특히 다음 네 축은 장 확장 또는 심화 페이지가 필요합니다.

1. `SEO → SERP → AIO → GPT/Claude/Perplexity 답변 환경`으로 이어지는 검색 환경 정의
2. `schema/JSON-LD/Product/Organization/Article/FAQ/Breadcrumb`를 별도 심화 흐름으로 다루는 구조화 데이터 축
3. `커머스 GEO/AIO/AI 구매 에이전트`를 산업별 한 페이지가 아니라 독립 심화 장으로 다루는 축
4. HaloX 블로그/글로서리/스터디 노트를 각 장의 참고 링크와 용어 정의에 더 촘촘히 연결하는 축

## 1장부터 흐름 리뷰

| 구간 | 현재 역할 | 유지 | 보강 필요 |
|---|---|---|---|
| 00장 | GEO 입문/용어 경계 | 유지 | SEO는 SERP 중심, AIO는 검색 결과 안의 AI 답변, GEO는 GPT/Claude/Perplexity까지 포함하는 답변 시장이라는 단계 정의 강화 |
| 01장 | SEO 키워드에서 AI 질문 시장으로 | 유지 | 키워드 → SERP 의도 → AI Overview 질문 → GPT/Claude 프롬프트로 확장되는 예시 강화 |
| 02장 | mention/source/citation 측정 | 유지 | 질문셋 포션, 검색 TOP10과 AI 답변 교차율, 인용 안정성, 모델별 관측 차이 보강 |
| 03장 | Fan-out과 질문 확장 | 유지 | 산업별 fan-out 예시를 더 넣기. 커머스/로컬/PR/금융 별 질문맵 필요 |
| 04장 | AI가 읽기 좋은 콘텐츠 구조 | 유지 | 스키마 자체는 04-02만으로는 부족. schema는 06장과 함께 별도 심화 페이지 후보 |
| 05장 | 답변 근거/화면 인용/엔티티 | 유지 | 위키/PR/언론/UGC/리뷰/커뮤니티/YouTube/네이버 블로그 역할표 강화 |
| 06장 | 테크니컬 GEO | 유지 | Schema 심화, Product/Organization/Article/FAQ/Breadcrumb 타입별 점검표, sitemap/canonical/redirect 실무 플로우 강화 |
| 07장 | 산업별 GEO | 확장 필요 | 커머스는 07-02 한 페이지로 부족. 독립 장 후보. PR/뉴스룸/로컬/금융도 심화 가능 |
| 08장 | 글로벌/영문 GEO | 유지 | 영문 카테고리 자산/Reddit/디렉터리/리뷰 DB와 한국어 질문의 연결 강화 |
| 09장 | 도구/파트너/리포트 검증 | 유지 | 도구 검증 질문과 리포트 샘플 강화. 단, 공개본에서는 세일즈 언어 과다 노출 주의 |
| 10장 | 4주 실행 로드맵 | 유지 | 강의자료용 별도 패키지 문서로 분리하는 편이 안전. 공개 WikiDocs 본문은 독자 실행형 유지 |

## 장 추가 판단

### 11장 후보: 커머스 GEO와 AI 구매 에이전트

추가 가치가 큽니다. 현재 07-02는 커머스 관점을 소개하지만, Obsidian의 `AI_GEO_커머스_보고서`, `AI 구매 에이전트 시대, 커머스는 무엇을 준비해야 할까`, `AI 고객을 위한 상품 정보 구조화` 블로그 축을 담기에는 얇습니다.

권장 구조:

| 페이지 | 다룰 내용 | 원천 소스 |
|---|---|---|
| 11. 커머스 GEO와 AI 구매 에이전트 | 클릭/검색 노출에서 AI 구매 후보/결제 가능성으로 이동하는 큰 그림 | AI_GEO_커머스_보고서 |
| 11-01. SEO/SERP/AIO/GPT가 커머스에서 갈라지는 지점 | SERP 노출, AI Overview, ChatGPT/Claude/Perplexity 추천 환경 차이 | 글로서리 SERP/AIO/GEO, GEO vs SEO vs AEO 블로그 |
| 11-02. AI 고객을 위한 상품 정보 구조 | 상품명/가격/재고/옵션/배송/환불/리뷰/정책 데이터 | ai-customer-product-info-structure |
| 11-03. Product schema와 merchant feed는 무엇을 보완하나 | Product/Offer/Review schema, merchant feed, 정책 문서, llms.txt의 역할 분리 | schema-markup-practical, Product structured data |
| 11-04. AI 구매 에이전트 시대의 리스크와 체크리스트 | 잘못된 가격/재고/정책 인용, 결제/환불/책임 소재, 운영 점검표 | agentic-commerce-geo, Project Vend/Deal 공개 사례 |

이 장은 `07장 산업별 GEO` 아래 한 페이지로 두기보다, 07-02에서는 “왜 별도 장으로 넘어가야 하는가”만 설명하고 11장에서 깊게 다루는 편이 좋습니다.

### Schema 심화는 어디에 둘까

스키마만으로도 한 장이 될 수 있지만, 지금 당장 독립 장으로 빼면 04장/06장과 중복될 위험이 있습니다. 우선은 다음처럼 분산하는 편이 좋습니다.

| 위치 | 역할 |
|---|---|
| 04-02 | FAQ/표/schema가 콘텐츠 의미를 보존하는 원리 |
| 06-05 | schema/title/canonical/본문/내부 링크의 의미 일치 점검 |
| 신규 06-06 후보 | Schema 타입별 실전 점검표: Organization/Article/Product/FAQ/Breadcrumb/Review |
| 신규 11-03 후보 | Product schema와 merchant feed를 커머스 문맥에서 심화 |

## 우선순위

1. P0: 00-02/01장에 `SEO는 SERP, AIO는 SERP 안의 AI 답변, GEO는 GPT/Claude/Perplexity까지 포함한 답변 시장` 정의를 보강합니다.
2. P0: `EXPANSION_BACKLOG.md`에 11장 커머스 심화 장과 06-06 schema 심화 후보를 추가합니다.
3. P1: 07-02를 커머스 독립 장으로 연결되는 브리지 페이지로 보강합니다.
4. P1: 신규 11장 초안을 추가합니다. 단, WikiDocs page_id가 생긴 뒤 내부 링크를 한 번 더 정리해야 합니다.
5. P2: 02장 측정/05장 오프사이트/06장 기술 체크리스트를 장별로 재보강합니다.

## 공개 전환 주의

- 내부 고객명/파트너명/비공개 수치/Slack 링크는 넣지 않습니다.
- Project Vend/Deal 등 공개 사례는 원문 세부를 과장하지 않고 “가능성과 리스크를 보여준 공개 실험”으로만 씁니다.
- 커머스 장에서도 “결제가 곧 AI로 대체된다”처럼 단정하지 않습니다. 핵심은 `상품 데이터가 AI가 비교/추천/구매 후보로 다룰 만큼 명확한가`입니다.
