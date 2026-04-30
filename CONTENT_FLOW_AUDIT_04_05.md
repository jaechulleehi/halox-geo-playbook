## 04장/05장 연결 재점검 메모

### 진단

로이드 피드백 기준으로 4장과 5장을 다시 보면, 4장은 콘텐츠 구조 자체는 보강되어 있었지만 3장에서 재정의한 `AI query fan-out`과의 연결이 더 분명해야 했습니다. 5장은 source/citation/entity 자료가 꽤 들어가 있었지만, 4장에서 만든 owned content가 왜 외부 source/citation/entity 전략으로 이어지는지 초반 브릿지가 약했고 일부 본문 링크가 GitHub 로컬 파일명으로 남아 있었습니다.

### 정리한 개념 경계

| 구간 | 맡는 일 | 산출물 |
|---|---|---|
| 03장 | AI가 한 질문을 어떤 하위 판단으로 fan-out하는지 추정 | AI 검색 패턴/fan-out 노드 |
| 04장 | fan-out 노드에 답하는 자사 페이지 구조를 만든다 | Answer-first, H2, 표, FAQ, schema 후보, 내부 링크 |
| 05장 | 그 자사 페이지가 웹 전체의 source/citation/entity 신호와 연결되는지 본다 | source/citation 진단표, 엔터티 메시지 하우스, 오프사이트 source map |
| 06장 | 콘텐츠와 출처가 실제로 발견/렌더링/구조화되는지 기술 검증 | crawl/render/schema/canonical/sitemap 체크 |

### 이번 보강 내용

- 04 parent에 `AI fan-out 노드 → 목표 질문 → 첫 답변/표/FAQ/schema/source → 재측정` 흐름을 명확히 추가.
- 04장과 05장의 역할 경계를 `owned content 구조화`와 `source/citation/entity 검증`으로 분리.
- 04-01에 fan-out 노드별 첫 답변 번역표 추가.
- 04-02에 FAQ/표/schema가 05장의 외부 신호로 이어지는 기준표 추가.
- 04-03에 리라이트 후 05장으로 넘겨야 하는 조건 추가.
- 05 parent에 03→04→05 연결 모델과 04장에서 넘어오는 검증 질문 추가.
- 05-01/05-02/05-03에 각각 04장 산출물과 source/citation/entity/offsite source map의 관계 추가.
- 05장 로컬 `.md` 본문 링크를 WikiDocs page ID 링크로 정리.
- `SEO_GEO.md`의 03장 제목/역할을 최신 fan-out 개념으로 갱신.

### 남은 점검 후보

- 06장은 04/05에서 넘긴 schema, canonical, 렌더링, 크롤러 접근성 항목을 받아야 하므로 다음 테크니컬 점검 때 다시 연결을 맞춰야 합니다.
- 05-06~05-10은 이미 깊이가 있지만, 5장 전체 재검증 후 일부 문장/링크/중복은 추가 미세정리 후보입니다.
