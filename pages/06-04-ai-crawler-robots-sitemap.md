## AI 크롤러 접근성과 GEO robots/sitemap 점검

![AI 크롤러 접근성과 robots sitemap](../assets/images/page-heroes/halox-geo-06-04-ai-crawler-robots-sitemap-hero.png)

robots.txt와 sitemap은 오래된 SEO 기본처럼 보이지만, GEO에서도 출발점입니다. AI와 검색엔진이 공식 URL을 발견하거나 접근하지 못하면 좋은 콘텐츠, schema, 외부 source가 있어도 citation 후보가 되기 어렵습니다.

이 페이지의 목표는 모든 bot을 무조건 허용하자는 것이 아닙니다. 어떤 URL은 열어야 하고, 어떤 URL은 막아야 하며, 어떤 대표 문서를 sitemap으로 안내해야 하는지 운영 기준을 만드는 것입니다.

[TOC]

## robots는 접근 정책이고 sitemap은 발견 지도다

robots.txt는 crawler 접근 정책을 알려주고, sitemap은 발견해야 할 URL을 알려줍니다. 둘이 서로 다른 신호를 주면 AI와 검색엔진은 대표 URL을 안정적으로 이해하기 어렵습니다.

| 항목 | 확인할 내용 | 흔한 문제 |
|---|---|---|
| robots.txt | 차단/허용 경로 | 중요한 자료실이나 블로그가 막힘 |
| robots meta | 페이지 단위 색인 정책 | noindex가 남아 있음 |
| sitemap | 대표 URL 목록 | 새 리포트/뉴스룸 URL 누락 |
| HTTP 상태 | 접근 가능 여부 | 404/5xx/리다이렉트 체인 |
| 내부 링크 | 사이트 안의 발견 경로 | 고립 페이지가 됨 |

## HaloX 사이트 진단에서 볼 순서

사이트 진단의 Pages 탭에서 HTTP 상태, 메타 상태, SEO/GEO 점수를 함께 봅니다. 먼저 핵심 URL이 정상 응답하는지 확인합니다.

Issues에서는 robots, noindex, canonical, sitemap 누락처럼 발견/접근을 막는 이슈를 우선 처리합니다. 콘텐츠 품질 이슈보다 앞에 두는 이유는 crawler가 페이지를 보지 못하면 콘텐츠 개선이 측정되지 않기 때문입니다.

인용 추적에서 공식 URL이 계속 빠지는 질문은 sitemap과 robots를 다시 봅니다. 특히 뉴스룸, 자료실, 캠페인, 상품 상세처럼 새로 만든 페이지가 누락되기 쉽습니다.

![AI crawler 접근성 점검 흐름](../assets/images/body-figures/halox-geo-06-04-ai-crawler-access-route-map-codex-only.png)

*robots와 sitemap 점검은 crawler 접근 정책과 대표 URL 발견 경로를 맞추는 작업이다.*

## 가상 기업 AcmeGEO 예시

AcmeGEO는 리포트 예시 페이지를 만들었지만 sitemap에 넣지 않았고, 자료실 경로 일부가 robots에서 차단되어 있습니다. 공식 URL이 AI 답변에 거의 citation으로 잡히지 않고 외부 블로그만 반복됩니다.

먼저 sitemap에 대표 URL을 넣고, 차단 정책을 검토합니다. 그다음 내부 링크를 제품 페이지와 뉴스룸에서 연결하고, 사이트 진단으로 HTTP 상태와 noindex 여부를 확인합니다.

## 정리 양식

```text
핵심 URL:
HTTP 상태:
robots.txt 정책:
robots meta 상태:
sitemap 포함 여부:
내부 링크 경로:
차단해야 할 URL:
열어야 할 URL:
재측정 질문:
```

## 다음 흐름

접근 경로가 정리되면 AI가 페이지 내용을 어떤 구조로 이해하는지 봐야 합니다. 이어서 [Schema와 내부 링크로 AI 이해도 높이기](https://wikidocs.net/346394)를 읽습니다.
