## AI 크롤러 접근성과 robots/sitemap 점검법

![AI 크롤러 접근성과 robots sitemap](../assets/images/page-heroes/halox-geo-06-04-ai-crawler-robots-sitemap-hero.png)

AI 크롤러 접근성은 “허용/차단”만의 문제가 아닙니다. 핵심 URL이 sitemap과 내부 링크로 발견되고, robots.txt가 의도와 다르게 막지 않으며, 페이지 안 링크가 실제 href로 연결되는지 함께 봐야 합니다.

GEO에서는 특히 source/citation 후보가 될 페이지를 우선 점검합니다. 제품 소개, 리포트 예시, 용어사전, 비교 글, 뉴스룸, 사례 페이지가 여기에 해당합니다.

[TOC]

## robots.txt와 sitemap의 역할

robots.txt는 크롤러 접근 규칙을 알려주고, sitemap은 중요한 URL 목록을 알려줍니다. 둘 다 직접 순위를 올리는 마법 장치가 아니라 발견과 접근을 돕는 기본 장치입니다.

```text
User-agent: *
Allow: /
Sitemap: https://example.com/sitemap.xml
```

sitemap은 핵심 URL이 빠지지 않도록 관리합니다.

```xml
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://example.com/ko/glossary/generative-engine-optimization</loc>
    <lastmod>2026-05-03</lastmod>
  </url>
</urlset>
```

## 크롤 가능한 링크를 확인한다

내부 링크가 버튼 클릭 이벤트로만 연결되고 실제 href가 없으면 크롤러가 관계를 이해하기 어려울 수 있습니다. 중요한 링크는 HTML에서 실제 URL로 보여야 합니다.

| 링크 상태 | 판단 |
|---|---|
| 실제 href 링크 | 좋음 |
| 클릭 이벤트만 있고 href 없음 | 점검 필요 |
| 로그인 후에만 보이는 링크 | public source 후보로 약함 |

![AI 크롤러 발견 경로 점검](../assets/images/body-figures/halox-geo-06-04-ai-crawler-access-route-map-codex-only.png)

*robots, sitemap, 내부 링크는 핵심 URL이 발견되는 경로를 만든다.*

## 핵심 URL 발견 경로를 기록한다

```text
핵심 URL:
sitemap 포함 여부:
robots 허용 여부:
내부 링크 진입 경로:
외부 출처 링크:
canonical:
차단/누락 의심 지점:
```

이 기록이 있어야 개발팀에 “크롤이 안 되는 것 같다”가 아니라 “이 URL이 sitemap에는 있으나 주요 허브에서 내부 링크가 없다”처럼 구체적으로 요청할 수 있습니다.

## 다음 흐름

URL을 발견할 수 있다면 [Schema와 내부 링크](https://wikidocs.net/346394)에서 페이지의 의미 관계를 더 명확히 만드는 방법을 봅니다.
