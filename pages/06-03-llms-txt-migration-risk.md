## llms.txt와 사이트 이전 리스크 관리

![llms.txt와 사이트 이전 리스크](../assets/images/page-heroes/halox-geo-06-03-llms-txt-migration-risk-hero.png)

llms.txt는 AI가 참고하면 좋을 문서와 사이트 구조를 안내하기 위한 파일로 논의됩니다. 다만 llms.txt 하나로 GEO가 해결되지는 않습니다. 핵심 URL의 콘텐츠, 내부 링크, sitemap, robots, canonical이 먼저 맞아야 합니다.

사이트 이전은 더 조심해야 합니다. URL이 바뀌면 기존 source/citation 후보, 외부 링크, 검색 결과, AI 답변의 기억이 한동안 흔들릴 수 있습니다.

[TOC]

## llms.txt는 보조 안내다

간단한 형태는 아래처럼 생각할 수 있습니다.

```text
AcmeGEO

AI search visibility analysis platform for B2B SaaS teams.

Key pages
- Product overview: https://example.com/ko/product
- GEO report sample: https://example.com/ko/report-sample
- Glossary: https://example.com/ko/glossary/generative-engine-optimization
```

이 파일은 중요한 페이지를 알려주는 보조 신호입니다. 하지만 페이지 자체가 얕거나, sitemap에서 빠졌거나, robots로 막혀 있으면 효과를 기대하기 어렵습니다.

## 해결하는 것과 못 하는 것

| 구분 | 판단 |
|---|---|
| 핵심 문서 안내 | 도움 될 수 있음 |
| 브랜드 설명 정리 | 보조 역할 가능 |
| 색인/크롤링 문제 해결 | llms.txt만으로 해결 안 됨 |
| 잘못된 canonical 수정 | 별도 기술 조치 필요 |
| 오래된 외부 설명 정정 | PR/디렉터리/콘텐츠 정리 필요 |

## 사이트 이전에서 자주 생기는 문제

사이트 이전은 GEO 관점에서 source/citation 후보 URL을 다시 연결하는 작업입니다. 다음 문제가 자주 생깁니다.

- 301 리디렉션이 일부 URL에만 적용됨
- canonical이 이전 URL 또는 잘못된 대표 URL을 가리킴
- sitemap에 새 URL과 오래된 URL이 섞임
- 내부 링크가 예전 경로를 유지함
- 주요 외부 출처가 오래된 URL을 계속 인용함

![llms.txt와 사이트 이전 점검 보드](../assets/images/body-figures/halox-geo-06-03-llms-txt-migration-risk-board-codex-only.png)

*llms.txt는 보조 안내이고, 사이트 이전은 source/citation 후보 URL을 다시 연결하는 작업이다.*

## 이전 전후 재측정

사이트 이전 전에는 핵심 질문군과 citation 후보 URL을 기록합니다. 이전 후에는 같은 질문으로 브랜드 mention, source, citation, 검색 결과 URL이 어떻게 바뀌었는지 봅니다.

```text
이전 전 핵심 URL:
이전 후 대응 URL:
301 상태:
canonical:
sitemap 포함:
내부 링크 수정:
외부 출처 수정 요청:
재측정 질문:
```

## 다음 흐름

URL 발견과 접근성을 더 구체적으로 보려면 [AI 크롤러 접근성과 robots/sitemap 점검법](https://wikidocs.net/346393)을 읽습니다.
