## 06장 테크니컬 GEO 점검 메모

### 진단

06장은 이미 CSR/SSR, llms.txt, robots/sitemap, schema, Google 공식 도구, 메타 정보까지 폭이 넓게 잡혀 있었습니다. 다만 로이드가 지적한 “스키마가 실제로 어떻게 생겼는지, Google에서는 어떻게 정의하는지, Organization/바이오/FAQ schema를 어떻게 구분하는지” 관점에서는 04/05장과 06장의 연결, schema 타입 선택 기준, 도구 결과를 실행 티켓으로 바꾸는 흐름을 더 선명하게 해야 했습니다.

### 보강한 개념 경계

| 장 | 맡는 일 | 06장에서 이어받는 질문 |
|---|---|---|
| 04장 | Answer-first/표/FAQ/schema 후보로 자사 콘텐츠를 구조화 | 이 구조가 실제 HTML/DOM/JSON-LD에 남는가 |
| 05장 | source/citation/entity/offsite evidence를 설계 | source 후보 URL과 entity 설명이 robots/sitemap/canonical/schema에서 안정적인가 |
| 06장 | 발견/접근/렌더링/schema/meta/canonical 검증 | 개발팀이 실행할 URL별 티켓으로 바뀌는가 |

### 이번 보강 내용

- 06 parent의 첫 설명과 비교표를 `04 콘텐츠 구조 → 05 source/entity → 06 기술 검증` 흐름으로 재정리.
- 06 parent의 공개 독자 관점에 맞지 않는 `책` 행을 `독자 실행`으로 변경.
- 06-01의 10분 기본 점검표를 FAQ 뒤가 아니라 개념 설명 뒤쪽으로 이동해 읽는 흐름 정리.
- 06-03의 `llms.txt와 사이트 이전을 함께 보는 이유`를 참고 링크/FAQ 뒤가 아니라 개념 앞쪽으로 이동해 중복 흐름 정리.
- 06-05에 schema와 내부 링크를 함께 보는 이유, Organization/Person/FAQ/Product 조합별 좋은/약한 상태 추가.
- 06-06에 Google 공식 도구 결과를 개발/콘텐츠 티켓으로 바꾸는 표 추가.
- 06-07에 Organization/Person/FAQ/Product 타입 구분 빠른 기준과 Product/SoftwareApplication JSON-LD 예시 추가.

### 다음 점검 후보

- 06장 이후 07장으로 넘어갈 때 업종별로 어떤 schema/technical issue를 우선하는지 연결을 더 볼 수 있습니다.
- 11장 커머스/Product schema와 12장 로컬/NAP/LocalBusiness는 06장의 기술 기준을 업종별로 확장하는 후속 점검 후보입니다.
