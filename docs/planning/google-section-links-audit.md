# Google 검색결과 페이지 섹션 링크 전수 점검

## 결론

- 구글 검색결과의 작은 버튼형 링크는 구조화 데이터 리치 리절트보다 페이지 내 섹션 링크/사이트링크에 가깝다.
- WikiDocs HTML에서 `[TOC]`는 `<div class="toc"><a href="#...">...</a></div>`와 본문 헤딩 id로 변환되어 구글이 섹션 구조를 이해하기 쉽다.
- 이번 점검에서는 TOC.md에 등록된 모든 pages 문서에 `[TOC]`가 없었고, 전체 페이지에 도입부 뒤 `[TOC]`를 추가했다.

## 적용 기준

1. 첫 답변/도입부는 그대로 둔다.
2. 두 번째 `##` 헤딩이 시작되기 직전에 `[TOC]`를 넣는다.
3. 본문 H1은 사용하지 않는다.
4. 검색결과에 노출되면 좋은 문구는 `##`/`###` 헤딩으로 직접 쓴다.

## 수정 결과

- 대상 페이지: 88개
- `[TOC]` 추가 페이지: 88개
- 기존 `[TOC]` 보유 페이지: 0개

## `[TOC]` 추가 파일

- `pages/00-chapter-0.md`
- `pages/00-01-what-is-geo.md`
- `pages/00-02-geo-seo-aeo-aio.md`
- `pages/00-03-ai-search-difference.md`
- `pages/00-04-how-to-use-this-book.md`
- `pages/01-chapter-1.md`
- `pages/01-01-seo-keywords-still-matter.md`
- `pages/01-02-serp-analysis-content-gap.md`
- `pages/01-03-search-intent-ai-question.md`
- `pages/01-04-seo-content-structure-answer-first.md`
- `pages/01-05-onpage-seo-promise-proof.md`
- `pages/02-chapter-2.md`
- `pages/02-01-chatgpt-brand-visibility.md`
- `pages/02-02-perplexity-ai-overviews-citation.md`
- `pages/02-03-mention-source-citation.md`
- `pages/02-04-ai-search-report.md`
- `pages/03-chapter-3.md`
- `pages/03-01-fan-out-question-map.md`
- `pages/03-02-question-type-portfolio.md`
- `pages/03-03-content-gap-from-questions.md`
- `pages/04-chapter-4.md`
- `pages/04-01-answer-first-content.md`
- `pages/04-02-faq-schema-table-structure.md`
- `pages/04-03-geo-content-rewrite-checklist.md`
- `pages/05-chapter-5.md`
- `pages/05-01-source-citation-difference.md`
- `pages/05-02-entity-consensus-offsite.md`
- `pages/05-03-offsite-source-map.md`
- `pages/05-04-channel-source-strategy.md`
- `pages/05-05-reputation-risk-ai-answer.md`
- `pages/05-06-wiki-directory-entity-management.md`
- `pages/05-07-pr-media-trust-signal.md`
- `pages/05-08-reddit-community-usage-signal.md`
- `pages/05-09-external-blog-syndication-strategy.md`
- `pages/05-10-offsite-entity-operations-checklist.md`
- `pages/06-chapter-6.md`
- `pages/06-01-technical-geo-checklist.md`
- `pages/06-02-csr-ssr-rendering.md`
- `pages/06-03-llms-txt-migration-risk.md`
- `pages/06-04-ai-crawler-robots-sitemap.md`
- `pages/06-05-schema-internal-link-structure.md`
- `pages/06-06-google-seo-geo-validation-tools.md`
- `pages/06-07-schema-type-checklist.md`
- `pages/06-08-meta-canonical-snippet-checklist.md`
- `pages/07-chapter-7.md`
- `pages/07-01-b2b-saas-geo.md`
- `pages/07-02-commerce-platform-aio.md`
- `pages/07-03-local-specialist-geo.md`
- `pages/07-04-pr-newsroom-entity-geo.md`
- `pages/07-05-finance-regulated-geo.md`
- `pages/07-06-campaign-url-citation-tracking.md`
- `pages/08-chapter-8.md`
- `pages/08-01-english-category-assets.md`
- `pages/08-02-locale-hreflang-geo.md`
- `pages/08-03-global-source-map.md`
- `pages/09-chapter-9.md`
- `pages/09-01-geo-agency-checklist.md`
- `pages/09-02-geo-tool-report-criteria.md`
- `pages/09-03-geo-business-model.md`
- `pages/09-04-geo-proposal-structure.md`
- `pages/09-05-recurring-geo-report-product.md`
- `pages/09-06-geo-solution-recommendation.md`
- `pages/09-07-seo-tools-vs-geo-tools-comparison.md`
- `pages/10-chapter-10.md`
- `pages/10-01-week1-baseline-workshop.md`
- `pages/10-02-week2-fanout-gap-workshop.md`
- `pages/10-03-week3-content-source-workshop.md`
- `pages/10-04-week4-report-action-plan.md`
- `pages/11-chapter-11.md`
- `pages/11-01-agentic-commerce-search-shift.md`
- `pages/11-02-ai-customer-product-data.md`
- `pages/11-03-product-schema-merchant-feed.md`
- `pages/11-04-commerce-geo-risk-checklist.md`
- `pages/12-chapter-12.md`
- `pages/12-01-local-seo-local-geo-difference.md`
- `pages/12-02-nap-name-address-phone-checklist.md`
- `pages/12-03-naver-place-google-business-map-seo.md`
- `pages/12-04-review-offline-authority-strategy.md`
- `pages/12-05-local-question-set-conversion-checklist.md`
- `pages/12-06-medical-ad-review-risk.md`
- `pages/90-industry-geo-casebook.md`
- `pages/90-01-pr-agency-geo-service-case.md`
- `pages/90-02-campaign-url-citation-tracking-case.md`
- `pages/90-03-enterprise-newsroom-entity-hub-case.md`
- `pages/90-04-local-specialist-geo-case.md`
- `pages/90-05-finance-regulated-geo-case.md`
- `pages/90-06-commerce-platform-geo-case.md`
- `pages/91-halox-functional-mapping.md`

