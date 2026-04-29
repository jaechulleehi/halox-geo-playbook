## 테크니컬 GEO 기본 점검표

테크니컬 GEO는 AI가 콘텐츠를 발견하고 읽고 해석할 수 있게 만드는 기본 체력입니다. robots.txt, sitemap, canonical, schema, 응답 코드, 내부 링크, 페이지 속도, 렌더링 상태를 함께 봐야 합니다.

좋은 콘텐츠가 있어도 crawler가 접근하지 못하거나 본문을 읽지 못하면 GEO 성과를 설명하기 어렵습니다. 그래서 기술 점검은 개발팀만의 일이 아니라 콘텐츠팀, SEO팀, PR팀이 함께 보는 실행 체크리스트가 되어야 합니다.

## 먼저 볼 핵심 점검표

| 점검 항목 | 확인 질문 | GEO 영향 | 담당 |
|---|---|---|---|
| robots.txt | AI/검색 crawler를 불필요하게 막고 있지 않은가 | 발견/수집 가능성 | 개발/SEO |
| sitemap.xml | 핵심 블로그/글로서리/제품/뉴스룸 URL이 포함되는가 | 발견 우선순위 | 개발/콘텐츠 |
| canonical | 대표 URL이 정확히 지정되어 있는가 | 중복/구 URL 혼선 | 개발/SEO |
| 응답 코드 | 핵심 URL이 200, 이전 URL이 301로 정리되는가 | source 안정성 | 개발 |
| 내부 링크 | 질문별 핵심 페이지가 서로 연결되는가 | 의미 관계/탐색성 | 콘텐츠/SEO |
| schema | FAQ, Article, Product, Organization 정보가 구조화되는가 | 의미 해석 | 개발/콘텐츠 |
| 렌더링 | 초기 HTML에서 핵심 답변 재료가 보이는가 | 본문 수집 | 개발 |
| 속도/안정성 | 페이지가 느리거나 오류가 잦지 않은가 | crawler 효율 | 개발 |

## 사례로 이해하기

커머스/플랫폼 사례에서는 상품 페이지가 많아도 sitemap, canonical, schema가 맞지 않으면 AI가 어떤 페이지를 대표 source로 써야 하는지 헷갈릴 수 있습니다. 상품 정보는 최신인데 schema에는 오래된 가격이 남아 있거나, 카테고리 페이지가 canonical에서 빠지면 추천 답변의 정확도가 떨어집니다.

PR/뉴스룸 사례에서는 보도자료와 팩트시트가 많아도 sitemap에 핵심 URL이 빠져 있으면 source 후보가 약해집니다. AI가 오래된 기사만 반복한다면 콘텐츠 문제가 아니라 기술적 발견 경로 문제일 수 있습니다.

## HaloX 기능으로 설명하는 법

| 기능 흐름 | 설명 방식 |
|---|---|
| Citation 약한 URL 추출 | 인용이 약한 핵심 URL을 기술 점검 대상으로 고른다 |
| Search TOP10 vs AI answer overlap | 검색에는 노출되지만 AI 답변에는 빠지는 URL을 찾는다 |
| Source/Citation map | source 후보인데 citation이 약한 URL의 기술 원인을 본다 |
| 30일 재측정 | 기술 수정 후 같은 질문셋에서 citation 변화를 본다 |

## 실습 워크시트

| 입력 항목 | 작성 기준 |
|---|---|
| 점검 URL | 홈/제품/블로그/글로서리/뉴스룸/캠페인 URL |
| 점검 항목 | robots/sitemap/canonical/schema/internal link/rendering |
| 현재 상태 | 정상/주의/오류 |
| 증거 | 확인 URL, 화면, 응답 코드, view-source 메모 |
| GEO 영향 | AI 접근/인덱싱/source/citation/entity |
| 수정 담당 | 개발/마케팅/콘텐츠/PR |
| 완료 기준 | 수정 후 어떤 상태가 되어야 하는가 |

## 정리 양식

```text
도메인 / 점검일 / 핵심 URL / 오류 항목 / 증거 / GEO 영향 / 수정 담당 / 완료 기준 / 재점검일
```

## 작성 예시

예시는 `테크니컬 GEO 기본 점검표`를 가상의 사이트에 적용한 것입니다. 실제 점검에서는 URL, 증상, 개발 담당자, 수정 우선순위를 함께 남깁니다.

| 입력 항목 | 작성 예시 |
|---|---|
| 점검 URL | /ko/glossary/geo |
| 점검 항목 | sitemap.xml |
| 현재 상태 | 핵심 glossary 일부 누락 |
| 증거 | 사이트맵에서 GEO 용어 URL이 확인되지 않음 |
| GEO 영향 | 용어 정의 페이지가 AI 답변 근거로 쓰일 가능성이 낮아짐 |
| 수정 담당 | 개발팀이 사이트맵 생성 규칙을 확인한다 |
| 완료 기준 | glossary 핵심 URL이 sitemap과 내부 링크 허브에 모두 반영됨 |

## 완료 기준

- 핵심 URL별로 기술 이슈와 GEO 영향이 함께 적혀 있습니다.
- 수정 담당과 완료 기준이 보입니다.
- 기술 점검 결과가 HaloX 리포트의 source/citation 지표와 연결됩니다.
- 읽고 난 뒤 산출물로 쓰거나 실습 노트로 옮겨도 설명이 부족하지 않습니다.

## 참고 링크 패키지

이 실습은 HaloX의 [온페이지 SEO 체크리스트](https://haloxlabs.ai/ko/blog/on-page-seo-checklist-2026), [스키마 마크업 실전 가이드](https://haloxlabs.ai/ko/blog/schema-markup-practical), [llms.txt 완전 가이드](https://haloxlabs.ai/ko/blog/llms-txt-setup-guide)를 함께 보면 좋습니다.

기본 점검은 Google의 [robots.txt 소개](https://developers.google.com/search/docs/crawling-indexing/robots/intro), [sitemap 개요](https://developers.google.com/search/docs/crawling-indexing/sitemaps/overview), [크롤 가능한 링크 가이드](https://developers.google.com/search/docs/crawling-indexing/links-crawlable)를 함께 보며 확인합니다.

## 흔한 질문

**Q. 테크니컬 GEO는 SEO 기술 점검과 같은가요?**

겹치는 부분이 많습니다. 다만 GEO에서는 검색 순위뿐 아니라 AI 답변의 source/citation, entity 이해, answer quality까지 연결해 봅니다.

**Q. 모든 URL을 한 번에 점검해야 하나요?**

아닙니다. 먼저 HaloX 리포트에서 중요한 질문셋과 citation이 약한 URL을 고르고, 그 URL부터 기술 점검을 시작합니다.

## 다음 흐름

이전: [06. 테크니컬 GEO와 사이트 구조](https://wikidocs.net/346334) / 다음: [06-02. CSR/SSR 렌더링은 GEO에서 왜 중요한가](https://wikidocs.net/346354)
