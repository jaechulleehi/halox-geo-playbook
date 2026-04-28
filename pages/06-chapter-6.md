## 테크니컬 GEO와 사이트 구조

테크니컬 GEO는 AI가 콘텐츠를 발견하고, 읽고, 해석하고, 다시 인용할 수 있게 만드는 사이트의 기본 구조입니다. 좋은 글을 많이 써도 AI crawler가 접근하지 못하거나 핵심 본문이 렌더링 뒤에만 보이면 source/citation 성과를 안정적으로 만들기 어렵습니다.

이 장은 마케팅팀과 개발팀이 같은 체크리스트를 보고 이야기할 수 있도록 구성합니다. `robots.txt`, `sitemap.xml`, canonical, 응답 코드, CSR/SSR, schema, 내부 링크, llms.txt, 사이트 이전 리스크를 각각 따로 보되, 최종 판단은 “AI 답변에 쓸 수 있는 근거가 안정적으로 노출되는가”로 모읍니다.

## 테크니컬 점검 패키지

이 장의 흐름은 `기본 기술 점검 → 렌더링 확인 → llms.txt/이전 리스크 → AI crawler 접근성 → schema/내부 링크 구조화`입니다. 단순 개발 체크리스트가 아니라 GEO 리포트와 연결되는 점검표로 써야 합니다.

| 단계 | 핵심 질문 | 산출물 |
|---|---|---|
| 기본 점검 | AI가 핵심 페이지를 발견할 수 있는가 | robots/sitemap/canonical/응답 코드 점검표 |
| 렌더링 | 초기 HTML에서 답변 재료가 보이는가 | CSR/SSR/SSG 누락 콘텐츠 표 |
| llms.txt/이전 | 사이트 개편 후 기존 source/citation이 흔들리지 않는가 | 이전 전후 URL 매핑표 |
| AI crawler 접근성 | 주요 AI/검색 crawler가 막히지 않았는가 | crawler 접근 정책표 |
| Schema/내부 링크 | AI가 페이지 의미와 관계를 이해할 수 있는가 | schema/internal link 구조화 표 |

## 이 장에서 다루는 세부 페이지

- [06-01. 테크니컬 GEO 기본 점검표](https://wikidocs.net/346353)
- [06-02. CSR/SSR 렌더링은 GEO에서 왜 중요한가](https://wikidocs.net/346354)
- [06-03. llms.txt와 사이트 이전 리스크 관리](https://wikidocs.net/346355)
- [06-04. AI crawler 접근성과 robots/sitemap은 어떻게 점검할까](https://wikidocs.net/346393)
- [06-05. Schema와 내부 링크는 AI 이해를 어떻게 돕나](https://wikidocs.net/346394)

## 사례로 보는 테크니컬 GEO

커머스/플랫폼 사례에서는 상품 정보가 사용자에게는 보이지만 초기 HTML, schema, merchant feed, canonical에서 서로 다르게 보일 수 있습니다. 이 경우 AI는 가격, 재고, 리뷰, 카테고리 정보를 정확히 묶지 못하고 source로 쓰더라도 답변 품질이 흔들립니다.

뉴스룸/PR 사례에서는 기사와 팩트시트가 많아도 sitemap에 핵심 URL이 빠져 있거나, canonical이 엉켜 있거나, 사이트 개편 후 구 URL이 남아 있으면 AI 답변이 오래된 source를 붙잡을 수 있습니다.

글로벌/영문 GEO 사례에서는 locale, hreflang, canonical, 언어별 sitemap이 함께 맞아야 합니다. 한국어 글과 영문 글이 서로 다른 메시지를 주거나, 언어별 페이지 관계가 흐리면 AI 답변도 시장별로 일관되지 않습니다.

## HaloX 기능을 자연스럽게 붙이는 순서

테크니컬 GEO는 HaloX 리포트에서 발견한 문제를 개발 액션으로 바꾸는 연결 지점입니다.

1. 질문셋별로 citation이 약한 핵심 URL을 찾습니다.
2. 해당 URL의 robots/sitemap/canonical/응답 코드를 점검합니다.
3. 초기 HTML과 렌더링 후 화면에서 핵심 답변 재료가 같은지 봅니다.
4. schema와 내부 링크가 페이지의 의미와 관계를 설명하는지 확인합니다.
5. llms.txt와 핵심 문서 허브가 AI에게 우선 읽을 경로를 안내하는지 봅니다.
6. 수정 후 같은 질문셋으로 source/citation 변화를 재측정합니다.

이 흐름은 [02. GEO 측정 지표와 HaloX 분석 프레임](https://wikidocs.net/346342), [05. Source/Citation/Entity와 오프사이트 전략](https://wikidocs.net/346333), [10-04. 4주차: 실행 리포트와 30일 액션 플랜](https://wikidocs.net/346368)과 연결됩니다.

## 강의와 실무에서의 역할

| 사용 장면 | 이 장의 역할 | 산출물 |
|---|---|---|
| 강의 | 4주차 기술 점검 실습 | 테크니컬 GEO 체크리스트 |
| 실무 | 개발팀에 넘길 수정 요청 정리 | URL별 이슈/담당/완료 기준 |
| 제품 설명 | HaloX 리포트의 원인을 기술 액션으로 연결 | citation 약한 URL의 기술 진단표 |
| 이북 | 혼자 따라 할 수 있는 사이트 점검 워크북 | robots/sitemap/schema/llms.txt 실습표 |

## 다음 흐름

이 장은 앞선 [05. Source/Citation/Entity와 오프사이트 전략](https://wikidocs.net/346333)의 흐름을 이어받습니다. 기술 점검까지 마치면 [07. 산업별 GEO 전략](https://wikidocs.net/346335)으로 넘어가 업종별로 어떤 기술 요소가 더 중요한지 봅니다.
