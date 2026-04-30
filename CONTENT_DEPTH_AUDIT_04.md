## 04장 콘텐츠 깊이 보강 감사 메모

### 진단

04장은 03장에서 찾은 콘텐츠 갭을 실제 문서 구조로 바꾸는 장입니다. 기존 본문은 Answer-first, FAQ, 표, schema, 리라이트 체크리스트의 방향은 있었지만 `왜 이 구조가 AI 답변 재료가 되는가`, `Google 공식 문서 기준에서 schema를 어떻게 조심해야 하는가`, `기존 글을 어떤 순서로 고쳐야 하는가`가 더 깊게 필요했습니다.

### 반영한 소스

| 소스 | 4장 반영 위치 |
|---|---|
| `SOURCE_MAP.md` | 04장은 Answer-first/FAQ/표/schema/리라이트 체크리스트를 맡는다는 역할 기준 반영 |
| `BACKLINK_MAP.md` | AI 인용 콘텐츠, GEO 콘텐츠 구조, AI 선호 콘텐츠 구조 링크 반영 |
| HaloX `AI에게 인용되는 콘텐츠 만드는 법` | 04-01/04-03의 인용 가능 문장, source 연결, 리라이트 기준 반영 |
| HaloX `GEO 콘텐츠 구조화 가이드` | 04 parent/04-01/04-03의 본문 구조, 표, FAQ, source map 반영 |
| HaloX `AI 검색이 선택하는 콘텐츠의 5가지 공통점` | 04 parent/04-02의 정보 단위 구조화 기준 반영 |
| Google Search Central `Creating helpful content` | 독자에게 실제 도움이 되는 콘텐츠 기준 반영 |
| Google structured data intro / Article / FAQPage | schema는 본문을 대체하지 않고, Google 리치 결과를 보장하지 않는다는 기준 반영 |
| schema.org `Article`, `FAQPage` | 구조화 데이터 타입의 기본 개념과 JSON-LD 예시 반영 |
| Obsidian `LLM WIKI MAINTENANCE RULES` | TL;DR/Answer-first/표/FAQ/레퍼런스 링크 최소 요건 반영 |
| `PDF_WORKBOOK.md` | Answer-first 첫 문단, 표/FAQ 보강, source map 워크시트 반영 |

### 핵심 모델

```text
03장 콘텐츠 갭
→ 목표 질문 선택
→ 첫 답변 재작성
→ H2를 질문/판단 기준으로 정리
→ 표로 비교 기준 고정
→ FAQ로 후속 질문 보강
→ schema는 본문과 일치하는 범위에서 보조 신호로 사용
→ source/internal link 연결
→ 같은 질문셋으로 재측정
```

### 보강 포인트

- 04 parent: AI가 페이지를 읽는 과정을 `URL 발견 → 제목/설명 판단 → HTML/DOM 수집 → 텍스트 구조화 → 답변 합성`으로 정리.
- 04-01: Answer-first 첫 문단의 5요소와 before/after 리라이트 예시 보강.
- 04-02: FAQ/표/schema의 역할 분리, Google 공식 기준, FAQPage/Article JSON-LD 예시, schema 사용 금지 패턴 보강.
- 04-03: 기존 글을 GEO 콘텐츠로 바꾸는 7단계 리라이트 프로세스와 담당/완료 기준 표 보강.

### 다음 연결

04장에서 고친 문서가 실제 답변 근거와 화면 인용으로 이어지는지는 05장에서 source/citation 관점으로 확인합니다. schema, canonical, 렌더링, sitemap처럼 기술 검증이 필요한 항목은 06장으로 넘깁니다.
