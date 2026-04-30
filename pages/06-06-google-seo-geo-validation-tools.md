## Google 공식 도구로 SEO/GEO 기술 상태 점검하기

메타 정보, 리치 리절트, schema, 페이지 속도는 SEO에서만 중요한 항목이 아닙니다. GEO에서도 이 요소들은 AI가 페이지의 주제와 구조를 이해하고, 답변 근거(source)나 화면 인용(citation) 후보로 판단하는 데 영향을 줍니다.

이 페이지의 목적은 “점수를 높이는 법”이 아니라, Google 공식 문서와 도구를 기준으로 페이지가 검색엔진과 AI에게 읽히기 좋은 상태인지 확인하는 것입니다. 메타 정보가 무엇인지, 리치 리절트가 무엇인지, schema를 어떻게 세팅하고 검증해야 하는지, PageSpeed와 Search Console을 어떻게 함께 봐야 하는지 한 번에 점검합니다. title/meta description/canonical/robots meta를 더 깊게 점검해야 한다면 06-08의 메타 정보 실전 점검으로 분리해 봅니다.

[TOC]

## 메타 정보란 무엇인가

메타 정보는 페이지의 주제와 대표 설명을 검색엔진, 브라우저, 외부 서비스에 알려주는 기본 신호입니다. 사용자가 화면에서 본문을 읽기 전에 검색 결과, 공유 미리보기, 탭 제목 등에서 먼저 만나는 정보이기도 합니다.

GEO 관점에서는 메타 정보가 “이 페이지가 어떤 질문에 대한 답인지”를 압축해서 알려주는 첫 신호가 됩니다. title, meta description, canonical, robots, Open Graph 같은 정보가 본문과 다른 말을 하면 검색엔진도 AI도 페이지의 역할을 안정적으로 이해하기 어렵습니다.

| 항목 | 역할 | 좋은 상태 |
|---|---|---|
| title | 검색 결과와 브라우저 탭에 보이는 페이지 제목 | 핵심 질문/주제/브랜드가 자연스럽게 드러남 |
| meta description | 검색 결과 설명 후보로 쓰이는 요약 | 페이지의 답변 가치와 차별점이 1~2문장으로 보임 |
| canonical | 대표 URL 지정 | 중복 URL이 있어도 어느 URL을 기준으로 볼지 명확함 |
| robots meta | 색인/링크 추적 허용 여부 안내 | 중요한 페이지가 noindex 등으로 막혀 있지 않음 |
| Open Graph/Twitter Card | SNS/메신저 공유 미리보기 | 공유 제목/설명이 본문과 충돌하지 않음 |

## 메타 정보는 어떻게 세팅하면 좋은가

메타 정보는 키워드를 많이 넣는 칸이 아닙니다. 본문이 실제로 답하는 질문을 짧고 정확하게 요약하는 칸입니다.

| 항목 | 세팅 기준 | 피해야 할 상태 |
|---|---|---|
| title | “핵심 주제 + 독자 문제 + 브랜드/사이트명” 순서로 정리 | 모든 페이지가 같은 제목을 씀 |
| meta description | 본문에서 얻을 수 있는 답과 대상 독자를 명확히 씀 | 클릭 유도 문구만 있고 실제 내용이 없음 |
| canonical | 실제 대표 페이지 URL을 지정 | 필터/검색/임시 URL이 대표로 남음 |
| robots | 공개해야 할 페이지는 index/follow 상태 유지 | 핵심 글이 noindex로 배포됨 |
| OG 정보 | 공유될 때도 같은 메시지를 유지 | SEO title과 공유 title이 다른 주제를 말함 |

예를 들어 `GEO 뜻` 페이지라면 title은 “GEO 뜻: 생성형 엔진 최적화란 무엇인가”처럼 질문과 답의 범위가 보여야 합니다. meta description은 “GEO가 무엇인지, SEO/AEO/AIO와 어떻게 다른지, 실무에서 어떤 지표를 봐야 하는지 정리합니다”처럼 본문이 실제로 제공하는 답을 요약하는 편이 좋습니다.

## 리치 리절트란 무엇인가

리치 리절트는 Google 검색 결과에서 일반 파란 링크보다 더 풍부한 형태로 노출되는 검색 결과를 말합니다. FAQ, 리뷰, 상품 정보, 이벤트, 레시피, 조직 정보, breadcrumb 같은 구조화 데이터가 검색 결과 표현에 영향을 줄 수 있습니다.

중요한 점은 schema를 넣는다고 무조건 리치 리절트가 보장되는 것은 아니라는 점입니다. Google은 구조화 데이터를 이해에 활용할 수 있지만, 실제 검색 결과 노출 방식은 검색어, 품질, 정책, 페이지 상태에 따라 달라집니다. 따라서 목표는 “무조건 리치 리절트 만들기”가 아니라 “본문에 있는 정보를 검색엔진과 AI가 구조적으로 이해할 수 있게 만들기”입니다.

## schema는 어떻게 세팅하면 좋은가

Schema는 페이지의 의미를 기계가 읽기 쉬운 형태로 보조하는 구조화 데이터입니다. 보통 JSON-LD 방식으로 HTML에 넣습니다. GEO에서는 schema가 본문, title, canonical, 내부 링크와 같은 의미를 말하는지가 중요합니다.

| 페이지 유형 | 우선 검토할 schema | 세팅 기준 |
|---|---|---|
| 블로그/가이드 | Article, BlogPosting, FAQPage | 제목/설명/작성일/수정일/본문 주제가 일치해야 함 |
| 글로서리/정의 페이지 | DefinedTerm, FAQPage | 용어 정의와 관련 질문이 본문에 실제로 있어야 함 |
| 회사/브랜드 소개 | Organization, ProfilePage | 조직명, 로고, 공식 URL, 연락처, 외부 프로필이 본문과 일치해야 함 |
| 대표/전문가 바이오 | Person, ProfilePage, Article | 이름, 직함, 소속, 전문 분야, 저자 글이 공개 본문과 연결되어야 함 |
| 제품/SaaS 페이지 | Product, SoftwareApplication, FAQPage, BreadcrumbList | 기능, 가격, 대상, FAQ가 본문과 충돌하지 않아야 함 |
| 커머스 상품 | Product, Offer, Review, BreadcrumbList | 가격/재고/리뷰 정보가 상세페이지와 feed에서 일치해야 함 |
| 로컬/전문 서비스 | LocalBusiness, Review, FAQPage | 이름/주소/전화번호, 진료/서비스 범위, 후기 정책이 일관되어야 함 |
| 뉴스룸/보도자료 | NewsArticle, Organization | 회사명, 발행일, 팩트시트, 조직 정보가 명확해야 함 |

Schema 세팅에서 가장 위험한 패턴은 `schema에만 있고 본문에는 없는 정보`입니다. 검색엔진과 AI는 사용자에게 보이는 본문, HTML 텍스트, schema, title/canonical을 함께 봅니다. 구조화 데이터가 본문을 과장하거나 오래된 정보를 담고 있으면 오히려 신뢰 신호가 약해질 수 있습니다.

## Google 공식 문서를 읽을 때 구분할 것

Google 문서를 볼 때는 `지원되는 리치 리절트 유형`, `schema.org 문법`, `색인/크롤링 상태`, `검색 결과 제목/설명 생성 방식`을 나눠 읽어야 합니다. 이 네 가지를 한꺼번에 “스키마 문제”라고 부르면 개발팀에 넘길 액션이 흐려집니다.

| 구분 | 공식 문서/도구에서 보는 것 | 개발팀에 넘길 질문 |
|---|---|---|
| 구조화 데이터 개요 | Google이 구조화 데이터를 사용해 페이지 콘텐츠를 이해한다는 원칙 | 이 페이지의 핵심 정보가 JSON-LD로도 표현되어 있는가 |
| 리치 리절트 | Google 검색 결과에서 지원하는 특수 노출 유형 | 이 schema가 실제로 Google 지원 유형에 해당하는가 |
| schema.org 문법 | 타입/속성/중첩 구조가 유효한지 | `@type`, 필수/권장 속성, 중첩 객체가 맞는가 |
| 검색 결과 title/snippet | 검색 결과 제목/설명이 어떻게 선택될 수 있는지 | title/meta description/H1/본문 첫 문단이 같은 주제를 말하는가 |
| canonical/robots/sitemap | 대표 URL, 색인 허용, 발견 경로 | AI가 인용해야 할 대표 URL이 막히거나 중복되지 않았는가 |

GEO 관점에서 가장 중요한 것은 “도구 통과”가 아니라 “AI가 답변 근거로 써도 되는 대표 URL과 대표 설명이 일관적인가”입니다.

## Google 공식 도구로 점검하는 순서

기술 점검은 도구를 많이 돌리는 것보다 순서가 중요합니다. 먼저 색인과 대표 URL을 확인하고, 그다음 구조화 데이터와 리치 리절트, 마지막으로 페이지 속도와 사용자 경험을 확인합니다.

| 순서 | 확인 항목 | 사용할 도구/문서 | 통과 기준 |
|---|---|---|---|
| 1 | 색인 가능성 | Google Search Console URL 검사 | 핵심 URL이 색인 가능하고 막혀 있지 않음 |
| 2 | 검색 성과 | Search Console 성과 보고서 | 주요 검색어/페이지 노출과 클릭 흐름을 확인함 |
| 3 | 메타/canonical | 소스 보기, URL 검사, 검색 결과 확인 | title/description/canonical이 본문과 일치함 |
| 4 | 리치 리절트 | Rich Results Test | 지원되는 구조화 데이터가 오류 없이 읽힘 |
| 5 | schema 문법 | Schema Markup Validator | JSON-LD 문법과 타입이 유효함 |
| 6 | 페이지 속도 | PageSpeed Insights, Lighthouse | Core Web Vitals와 렌더링 병목을 확인함 |
| 7 | 크롤링 경로 | robots.txt, sitemap.xml | 핵심 URL이 발견 가능하고 차단되지 않음 |

## 공식 링크 패키지

아래 링크는 6장 실습에서 기준 문서로 함께 열어두면 좋습니다.

| 주제 | 공식 링크 | 볼 것 |
|---|---|---|
| 구조화 데이터 개요 | [Google 구조화 데이터 소개](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data) | Google이 구조화 데이터를 어떻게 이해하는지 |
| 리치 리절트 테스트 | [Rich Results Test](https://search.google.com/test/rich-results) | 현재 URL 또는 코드가 리치 리절트 대상인지 |
| 구조화 데이터 검증 | [Schema Markup Validator](https://validator.schema.org/) | schema.org 기준 문법과 타입 오류 |
| title link | [Google title link 문서](https://developers.google.com/search/docs/appearance/title-link) | 검색 결과 제목이 어떻게 생성되는지 |
| snippet | [Google snippet 문서](https://developers.google.com/search/docs/appearance/snippet) | meta description과 검색 결과 설명의 관계 |
| canonical | [중복 URL canonical 문서](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls) | 대표 URL 지정 기준 |
| robots.txt | [robots.txt 소개](https://developers.google.com/search/docs/crawling-indexing/robots/intro) | 크롤러 차단 여부 |
| sitemap | [sitemap 개요](https://developers.google.com/search/docs/crawling-indexing/sitemaps/overview) | 핵심 URL 발견 경로 |
| PageSpeed | [PageSpeed Insights](https://pagespeed.web.dev/) | Core Web Vitals와 성능 개선 힌트 |
| Search Console | [Search Console 성과 보고서](https://support.google.com/webmasters/answer/7576553) | 검색 노출/클릭/검색어 기준선 |

## GEO 관점으로 다시 해석하기

SEO 도구의 통과 결과가 곧 GEO 성과를 보장하지는 않습니다. 하지만 기본 기술 상태가 흔들리면 AI 답변 근거로 쓰일 가능성도 낮아집니다.

| SEO 점검 결과 | GEO에서 다시 볼 질문 |
|---|---|
| title/meta가 명확함 | AI가 이 페이지를 어떤 질문의 답으로 분류할 수 있는가 |
| schema 오류 없음 | schema와 본문이 같은 사실을 말하는가 |
| Rich Results Test 통과 | 구조화된 정보가 실제 본문에도 보이는가 |
| PageSpeed 점수 양호 | 핵심 본문과 표/FAQ가 빠르게 읽히는가 |
| Search Console 노출 있음 | AI 답변에서도 source/citation 후보로 등장하는가 |
| sitemap/robots 정상 | 핵심 허브와 하위 페이지가 모두 발견 가능한가 |

즉, 6장의 결론은 “Google 도구 점수가 좋다”가 아닙니다. 좋은 상태는 검색엔진이 발견하고, 사용자가 이해하고, AI가 답변 재료로 삼을 수 있는 구조가 함께 맞는 것입니다.

## 실습 워크시트

| 입력 항목 | 작성 기준 |
|---|---|
| 점검 URL | 홈/제품/블로그/글로서리/뉴스룸/상품/로컬 페이지 |
| 페이지 목적 | 어떤 질문에 답해야 하는 페이지인가 |
| title | 핵심 질문과 주제가 보이는가 |
| meta description | 본문 가치를 정확히 요약하는가 |
| canonical | 대표 URL이 맞는가 |
| schema 유형 | Article/FAQ/Product/Organization/LocalBusiness 등 |
| Rich Results Test | 통과/오류/경고 |
| Schema Validator | 통과/오류/경고 |
| PageSpeed | 모바일/데스크톱 주요 이슈 |
| Search Console | 색인 상태/주요 검색어/노출 페이지 |
| GEO 영향 | source/citation/entity 이해에 어떤 영향을 주는가 |
| 수정 액션 | 콘텐츠/개발/SEO 담당별 다음 작업 |

## 정리 양식

```text
URL / 페이지 목적 / title / meta description / canonical / schema 유형 / 리치 리절트 결과 / schema 오류 / PageSpeed 이슈 / Search Console 상태 / GEO 영향 / 수정 담당 / 재점검일
```

## 작성 예시

| 입력 항목 | 작성 예시 |
|---|---|
| 점검 URL | /ko/glossary/generative-engine-optimization |
| 페이지 목적 | GEO 뜻과 SEO/AEO/AIO 차이를 설명하는 정의 페이지 |
| title | GEO 뜻: 생성형 엔진 최적화란 무엇인가 |
| meta description | GEO의 의미, SEO와의 차이, AI 검색에서 봐야 할 지표를 정리합니다 |
| schema 유형 | Article, FAQPage, BreadcrumbList |
| 리치 리절트 결과 | FAQPage 경고 1개, 필수 오류 없음 |
| PageSpeed 이슈 | 모바일 LCP 개선 필요 |
| GEO 영향 | 정의 페이지가 AI 답변 source 후보가 되려면 본문 첫 문단과 FAQ 일치 필요 |
| 수정 액션 | FAQ 본문/schema 일치, 이미지 최적화, glossary 허브 내부 링크 추가 |

## 완료 기준

- 메타 정보가 무엇인지 설명할 수 있습니다.
- 리치 리절트와 schema의 관계를 구분할 수 있습니다.
- Google 공식 도구로 URL별 상태를 확인할 수 있습니다.
- title/meta/canonical/schema/본문이 같은 의미를 말하는지 점검했습니다.
- PageSpeed와 Search Console 결과를 GEO의 답변 근거(source)/화면 인용(citation) 관점으로 해석했습니다.

## 흔한 질문

**Q. schema만 넣으면 리치 리절트가 나오나요?**

아닙니다. schema는 리치 리절트의 필요 조건이 될 수 있지만 보장 조건은 아닙니다. Google 정책, 검색어, 페이지 품질, 본문 일치 여부, 사이트 신뢰도에 따라 실제 노출은 달라집니다.

**Q. meta description은 순위에 직접 영향을 주나요?**

meta description은 일반적으로 순위 요소라기보다 검색 결과 설명 후보와 클릭 판단에 영향을 주는 정보로 봐야 합니다. GEO에서는 페이지 주제를 요약하는 보조 신호로 함께 봅니다.

**Q. PageSpeed 점수가 낮으면 AI 답변에 안 나오나요?**

점수 하나로 단정할 수는 없습니다. 다만 느린 페이지, 렌더링이 늦게 되는 본문, 불안정한 서버 응답은 크롤링과 본문 수집 안정성을 떨어뜨릴 수 있습니다.

**Q. Google 도구만 보면 GEO 점검이 끝나나요?**

아닙니다. Google 도구는 기술 상태를 확인하는 기준입니다. GEO에서는 여기에 AI 답변에서의 mention, 답변 근거(source), 화면 인용(citation), 경쟁 출처를 함께 봐야 합니다.

## 다음 흐름

Google 공식 도구로 URL 상태를 확인했다면 [06-07. Schema 타입별 실전 점검표](https://wikidocs.net/346851)에서 Organization/Person/FAQ/Product를 실제 페이지 유형에 맞게 다시 확인하고, 메타 정보는 [06-08. 메타 정보 실전 점검](https://wikidocs.net/346855)의 title/meta description/canonical 점검표로 이어서 봅니다. 그다음 [07. 산업별 GEO 전략](https://wikidocs.net/346335)으로 넘어가 업종별로 어떤 schema와 기술 점검이 더 중요한지 봅니다. 커머스라면 [11-03. Product schema와 merchant feed 점검법](https://wikidocs.net/346599), 병원/오프라인 매장이라면 [12. 병원/오프라인 매장 SEO/GEO 전략](https://wikidocs.net/346606)도 함께 연결해 봅니다.
