## 테크니컬 GEO와 사이트 구조

![테크니컬 GEO와 사이트 구조 대표 이미지](../assets/images/page-heroes/halox-geo-06-chapter-6-hero.png)

테크니컬 GEO는 AI가 콘텐츠를 발견하고, 읽고, 해석하고, 다시 인용할 수 있게 만드는 사이트의 기본 구조입니다. 04장에서 좋은 콘텐츠 구조를 만들고 05장에서 답변 근거(source), 화면 인용(citation), 엔티티 신호를 설계했다면, 06장에서는 그 구조와 신호가 실제 HTML, 렌더링, schema, sitemap, robots, 내부 링크, canonical에서도 유지되는지 확인합니다.

좋은 글을 많이 써도 AI 크롤러가 접근하지 못하거나 핵심 본문이 렌더링 뒤에만 보이면 답변 근거/화면 인용 성과를 안정적으로 만들기 어렵습니다. 이 장은 마케팅팀과 개발팀이 같은 체크리스트를 보고 이야기할 수 있도록, 기술 항목을 GEO 리포트의 실행 액션으로 번역합니다.

`AcmeGEO`라는 이름은 설명을 위한 가상 기업명이며, 실제 고객 사례가 아닙니다.

[TOC]

## 04장/05장과 06장이 나뉘는 기준

04장은 “무엇을 어떤 구조로 써야 하는가”를 다룹니다. 05장은 그 콘텐츠가 웹 전체의 출처/인용/엔티티 신호와 연결되는지 봅니다. 06장은 그 콘텐츠와 신호가 실제로 크롤러와 AI에게 발견되고 읽히는지 확인합니다.

이 구분이 있어야 콘텐츠팀, PR/브랜드팀, 개발팀의 역할이 명확해집니다. 첫 문단이 좋은데 초기 HTML에는 없을 수 있고, 표는 유용한데 이미지로만 들어가 있을 수 있습니다. 공식 URL을 source 후보로 정했더라도 sitemap, canonical, robots, 내부 링크가 엉켜 있으면 AI가 안정적으로 발견하기 어렵습니다.

## 기술 점검은 개발 용어가 아니라 발견/해석의 문제다

테크니컬 GEO를 볼 때는 도구 이름을 외우기보다 네 가지 질문으로 시작하면 됩니다.

- **발견할 수 있는가**: robots, sitemap, 내부 링크, 응답 코드가 핵심 URL을 막지 않는가
- **읽을 수 있는가**: 초기 HTML, 렌더링 후 DOM, 표, FAQ, 본문 텍스트가 실제로 노출되는가
- **해석할 수 있는가**: title, meta description, heading, schema, canonical이 같은 주제를 말하는가
- **인용할 수 있는가**: 대표 URL이 안정적이고 오래된 URL/복제본/이전 URL과 충돌하지 않는가

![테크니컬 GEO 아키텍처](../assets/images/body-figures/halox-geo-06-chapter-6-technical-geo-architecture.png)

_콘텐츠 구조는 URL, HTML, schema, robots, sitemap, rendering 검증을 지나야 AI가 안정적으로 읽을 수 있습니다._

이 네 질문으로 보면 robots.txt, sitemap.xml, canonical, CSR/SSR, schema, llms.txt, 사이트 이전 리스크가 따로 노는 체크리스트가 아니라 하나의 흐름으로 연결됩니다.

## 2~5장 결과를 개발 티켓으로 바꾸는 법

6장은 기술 항목을 따로 외우는 장이 아니라 앞 장의 측정 결과를 URL별 개발/SEO 티켓으로 번역하는 장입니다. 2장에서 화면 인용이 약한 URL, 3장에서 source/citation 갭으로 분류된 노드, 4장에서 리라이트한 페이지, 5장에서 대표 source로 정한 URL을 기술적으로 안정화합니다.

| 앞 장의 신호 | 6장에서 확인할 것 | 개발/SEO 티켓 예시 |
|---|---|---|
| citation 후보 URL이 보이지 않음 | 색인, canonical, sitemap, 내부 링크 | 대표 URL sitemap 포함/canonical 수정 |
| source로 오래된 URL이 반복됨 | redirect, 301, robots meta | 구 URL 301 정리/robots meta 확인 |
| 본문은 있는데 답변 품질이 낮음 | 초기 HTML, H2, table, FAQ schema | 핵심 답변 HTML 본문화 |
| 엔티티 설명이 흔들림 | Organization/Person/Product schema | sameAs와 공식 URL 정렬 |
| 글로벌 URL이 혼선 | hreflang/canonical/locale | 언어별 alternate 링크 수정 |

AcmeGEO가 `GEO 리포트 예시` 페이지를 citation 후보로 키우려면 콘텐츠만 좋아서는 부족합니다. URL이 200으로 열리고, sitemap에 있고, canonical이 대표 URL을 가리키며, 첫 답변과 표가 초기 HTML에 있고, 내부 링크와 schema가 같은 주제를 말해야 합니다.

## 이 장을 읽는 순서

처음 점검한다면 [06-01. 테크니컬 GEO 기본 점검표](https://wikidocs.net/346353)에서 robots, sitemap, canonical, 응답 코드부터 봅니다. 본문이 화면에는 보이지만 AI가 잘 읽지 못하는 상황이 의심되면 [06-02. CSR/SSR 렌더링과 GEO 크롤링 리스크](https://wikidocs.net/346354)를 봅니다.

사이트 개편이나 URL 변경이 있었다면 [06-03. llms.txt와 GEO 사이트 이전 리스크 관리](https://wikidocs.net/346355)를 먼저 확인합니다. 크롤러 접근 정책은 [06-04. AI 크롤러 접근성과 GEO robots/sitemap 점검](https://wikidocs.net/346393), 구조화 데이터와 내부 링크는 [06-05. Schema와 내부 링크로 AI 이해도 높이기](https://wikidocs.net/346394)에서 다룹니다.

Google 공식 도구로 검증하려면 [06-06. Google 공식 도구 기반 SEO/GEO 기술 점검](https://wikidocs.net/346842), schema 타입별 점검은 [06-07. Schema 타입별 실전 점검표](https://wikidocs.net/346851), 메타 정보는 [06-08. 메타 정보 실전 점검](https://wikidocs.net/346855), 검색결과 섹션 링크와 리치 리절트 구분은 [06-09. 사이트링크와 리치 리절트 차이](https://wikidocs.net/346857)에서 이어집니다.

## 사례로 보는 테크니컬 GEO

커머스/플랫폼 사례에서는 상품 정보가 사용자에게는 보이지만 초기 HTML, schema, merchant feed, canonical에서 서로 다르게 보일 수 있습니다. 이 경우 AI는 가격, 재고, 리뷰, 카테고리 정보를 정확히 묶지 못하고 source로 쓰더라도 답변 품질이 흔들립니다.

뉴스룸/PR 사례에서는 기사와 팩트시트가 많아도 sitemap에 핵심 URL이 빠져 있거나, canonical이 엉켜 있거나, 사이트 개편 후 구 URL이 남아 있으면 AI 답변이 오래된 source를 붙잡을 수 있습니다.

글로벌/영문 GEO 사례에서는 locale, hreflang, canonical, 언어별 sitemap이 함께 맞아야 합니다. 한국어 글과 영문 글이 서로 다른 메시지를 주거나, 언어별 페이지 관계가 흐리면 AI 답변도 시장별로 일관되지 않습니다.

## HaloX 리포트와 개발 액션 연결하기

테크니컬 GEO는 HaloX 리포트에서 발견한 문제를 개발 액션으로 바꾸는 연결 지점입니다. 질문셋별로 citation이 약한 핵심 URL을 찾고, 해당 URL의 robots/sitemap/canonical/응답 코드를 점검합니다. 이어서 초기 HTML과 렌더링 후 화면에서 핵심 답변 재료가 같은지 보고, schema와 내부 링크가 페이지의 의미와 관계를 설명하는지 확인합니다.

수정 후에는 같은 질문셋으로 답변 근거/화면 인용 변화를 재측정합니다. 이 흐름은 [02. AI 검색 모니터링](https://wikidocs.net/346342), [05. 답변 근거/화면 인용/엔티티 전략](https://wikidocs.net/346333), [10-04. 4주차 GEO 실행 리포트와 30일 액션 플랜](https://wikidocs.net/346368)과 연결됩니다.

## 참고할 공식 기준

기술 점검은 HaloX의 [llms.txt 설정 가이드](https://haloxlabs.ai/ko/blog/llms-txt-setup-guide), [schema 실무 가이드](https://haloxlabs.ai/ko/blog/schema-markup-practical)와 연결됩니다. robots와 sitemap은 Google의 [robots.txt 소개](https://developers.google.com/search/docs/crawling-indexing/robots/intro), [sitemap 개요](https://developers.google.com/search/docs/crawling-indexing/sitemaps/overview)를 기준으로 함께 점검합니다.

메타 정보와 리치 리절트까지 확인할 때는 Google의 [구조화 데이터 소개](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data), [Rich Results Test](https://search.google.com/test/rich-results), [PageSpeed Insights](https://pagespeed.web.dev/), [Search Console 성과 보고서](https://support.google.com/webmasters/answer/7576553)를 함께 봅니다.

## 다음 흐름

이 장은 앞선 [05. 답변 근거/화면 인용/엔티티 전략](https://wikidocs.net/346333)의 흐름을 이어받습니다. 기술 점검까지 마치면 [07. 산업별 GEO 전략](https://wikidocs.net/346335)으로 넘어가 업종별로 어떤 기술 요소가 더 중요한지 봅니다.
