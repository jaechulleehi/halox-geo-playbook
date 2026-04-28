## 테크니컬 GEO와 사이트 구조

테크니컬 GEO는 AI가 콘텐츠를 발견하고, 읽고, 해석할 수 있게 만드는 기본 체력입니다. 좋은 글과 강한 외부 신호가 있어도 robots.txt가 막혀 있거나, sitemap이 부정확하거나, 중요한 본문이 렌더링되지 않으면 AI 검색에서 성과를 설명하기 어렵습니다.

이 장은 4주차 실습의 기술 점검 파트입니다. 목적은 개발자를 위한 체크리스트를 길게 늘리는 것이 아니라, 마케터와 콘텐츠 팀도 “어디서 막히는지”를 이해할 수 있게 만드는 것입니다.

HaloX의 [llms.txt 완전 가이드](https://haloxlabs.ai/ko/blog/llms-txt-setup-guide), [스키마 마크업 실전 가이드](https://haloxlabs.ai/ko/blog/schema-markup-practical), [온페이지 SEO 체크리스트](https://haloxlabs.ai/ko/blog/on-page-seo-checklist-2026)는 이 장의 실무 점검과 연결됩니다.

## 먼저 봐야 할 기술 신호

| 점검 항목 | 왜 보는가 | 위험 신호 |
|---|---|---|
| robots.txt | crawler 접근 허용 여부 확인 | AI crawler 또는 주요 경로 차단 |
| sitemap | 발견 가능한 URL 목록 확인 | 오래된 URL/누락 URL/리디렉션 URL 혼재 |
| canonical | 대표 URL 신호 확인 | 중복 페이지가 서로 다른 대표 URL 사용 |
| schema/JSON-LD | 구조화 데이터 확인 | 조직/제품/FAQ/Article 정보 누락 |
| SSR/CSR | 본문 렌더링 방식 확인 | JS 실행 전에는 핵심 본문이 비어 있음 |
| 속도/응답 코드 | 접근 안정성 확인 | 4xx/5xx/느린 응답/차단 페이지 |
| llms.txt | AI 친화 안내 파일 확인 | 핵심 문서 경로가 안내되지 않음 |

이 항목들은 GEO만의 새로운 기술이라기보다 SEO와 GEO의 공통 기반입니다. 차이는 “검색엔진이 색인할 수 있는가”에서 한 걸음 더 나아가 “AI 답변 재료로 안정적으로 읽히는가”를 본다는 점입니다.

## CSR과 SSR은 왜 중요한가

AI crawler와 검색 crawler가 모든 JavaScript를 사람 브라우저처럼 완벽하게 실행한다고 가정하면 위험합니다. 중요한 본문이 클라이언트 렌더링 이후에만 보인다면, 일부 환경에서는 내용이 비어 있거나 늦게 읽힐 수 있습니다.

그래서 GEO 점검에서는 실제 HTML 응답에 핵심 본문, 제목, 메타 정보, 구조화 데이터가 들어 있는지 확인해야 합니다. 특히 제품 상세, 카테고리 페이지, 블로그 본문, FAQ 영역은 렌더링 전후 차이를 비교해보는 것이 좋습니다.

## llms.txt는 만능이 아니다

llms.txt는 AI 시스템이 사이트의 중요한 문서와 정책을 이해하도록 돕는 안내 파일입니다. 하지만 llms.txt를 만들었다고 GEO가 자동으로 해결되지는 않습니다. 핵심 페이지 자체가 부실하거나, source/citation 신호가 없거나, robots 정책이 어긋나면 효과는 제한적입니다.

좋은 llms.txt는 다음 기준을 따릅니다.

- 핵심 개념/제품/문서/가격/정책 페이지를 선별한다.
- 중복되거나 오래된 페이지를 억지로 넣지 않는다.
- 사람에게도 이해되는 짧은 설명을 붙인다.
- sitemap, canonical, robots 정책과 충돌하지 않는다.
- 변경 후 AI 답변과 crawler 로그 변화를 함께 본다.

## 마이그레이션과 리디렉션 리스크

사이트 개편, CMS 이전, URL 변경은 GEO 이전에 SEO 리스크입니다. 잘못된 301 redirect, canonical 충돌, sitemap 누락, 삭제된 문서의 방치가 생기면 AI가 참고할 source도 흔들립니다.

특히 기존에 AI 답변에서 source/citation으로 쓰이던 URL을 바꿀 때는 더 조심해야 합니다. 단순히 새 URL을 만들고 끝내지 말고, 이전 URL에서 새 URL로의 이동, 내부 링크, sitemap 반영, Search Console 상태, 주요 AI 답변 변화까지 함께 확인해야 합니다.

## 4주차 테크니컬 점검표

| 단계 | 확인할 것 | 산출물 |
|---|---|---|
| 접근성 | robots.txt, 응답 코드, 차단 여부 | crawler 접근 체크 |
| 발견성 | sitemap, 내부 링크, orphan page | URL 발견성 목록 |
| 대표성 | canonical, redirect, 중복 URL | 대표 URL 정리표 |
| 구조성 | schema, heading, FAQ, breadcrumb | 구조화 데이터 체크 |
| 렌더링 | SSR/CSR, 본문 HTML 포함 여부 | 렌더링 비교 결과 |
| AI 안내 | llms.txt, 핵심 문서 경로 | AI 안내 파일 초안 |
| 변화 추적 | source/citation/mention 변화 | 30일 관찰 항목 |

## 흔한 실수

**Q. 테크니컬 GEO는 개발팀만 보면 되나요?**

아닙니다. 개발팀은 수정하고, 마케팅/콘텐츠 팀은 어떤 페이지가 중요한지 우선순위를 정해야 합니다.

**Q. Schema를 넣으면 AI가 바로 인용하나요?**

보장되지는 않습니다. schema는 이해를 돕는 신호이고, 본문 품질과 외부 신호가 함께 필요합니다.

**Q. robots.txt에서 AI crawler를 모두 허용하면 좋은가요?**

무조건은 아닙니다. 공개해도 되는 콘텐츠와 보호해야 할 콘텐츠를 구분해야 합니다. 허용 정책은 비즈니스와 보안 기준을 함께 봐야 합니다.

## 다음에 읽을 글

기술 기반을 확인했다면 업종별로 무엇이 달라지는지 봐야 합니다. 다음은 [산업별 GEO 전략](https://wikidocs.net/346335)입니다.
