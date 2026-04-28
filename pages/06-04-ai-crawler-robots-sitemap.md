## AI crawler 접근성과 robots/sitemap은 어떻게 점검할까

AI crawler 접근성 점검은 우리 사이트가 중요한 콘텐츠를 AI와 검색 시스템에 읽히도록 허용하고 있는지 확인하는 작업입니다. robots.txt, sitemap.xml, HTTP 응답 코드, 내부 링크가 함께 맞아야 합니다.

robots.txt를 열어두었다고 끝나는 문제가 아닙니다. 핵심 URL이 sitemap에 빠져 있거나, 차단 규칙이 특정 경로를 막거나, 서버가 crawler 요청에 불안정하게 응답하면 AI 답변의 source 후보가 약해질 수 있습니다.

## 먼저 구분할 것

| 구분 | 확인 질문 | 실무 판단 |
|---|---|---|
| 허용 정책 | 어떤 crawler를 허용/제한할 것인가 | 보안/저작권/노출 목적에 맞게 결정 |
| 핵심 경로 | 블로그/글로서리/제품/뉴스룸이 막히지 않았는가 | GEO source 후보는 접근 가능해야 함 |
| sitemap 품질 | 핵심 URL과 최신 URL이 들어 있는가 | 얇은 페이지보다 핵심 페이지 우선 |
| 응답 안정성 | crawler 요청에 200/301이 안정적인가 | 403/404/5xx 반복은 위험 |
| 내부 링크 | sitemap 외에도 사이트 안에서 연결되는가 | 허브/관련 글/카테고리 링크 보강 |

## 사례로 이해하기

뉴스룸 사례에서는 보도자료 경로가 robots.txt에서 실수로 막혀 있을 수 있습니다. 사람은 사이트 메뉴로 접근하지만 crawler는 차단되어 공식 source를 읽지 못하고 외부 기사만 참고할 수 있습니다.

커머스 사례에서는 상품 상세 페이지는 열려 있지만 필터/검색/카테고리 경로가 막혀 있거나 sitemap에서 빠질 수 있습니다. AI가 “어떤 제품군이 있는가”를 이해하려면 대표 카테고리와 핵심 상품 URL이 안정적으로 연결되어야 합니다.

글로서리 사례에서는 정의 페이지가 많아도 sitemap 갱신이 늦으면 신규 용어 페이지가 AI 답변 근거로 늦게 잡힙니다. GEO 용어/FAQ 페이지는 sitemap과 내부 링크 허브에 함께 넣는 것이 좋습니다.

## HaloX 기능으로 설명하는 법

| 기능 흐름 | 설명 방식 |
|---|---|
| Question-to-URL mapping | 질문셋별로 읽혀야 할 핵심 URL을 정한다 |
| Citation gap diagnosis | citation이 약한 URL의 접근성 문제를 찾는다 |
| Crawler access checklist | robots/sitemap/응답 코드/내부 링크를 함께 본다 |
| Re-measure report | 접근성 수정 뒤 source/citation 변화를 확인한다 |

## 실습 워크시트

| 입력 항목 | 작성 기준 |
|---|---|
| 핵심 URL | AI 답변에 근거로 쓰이길 원하는 URL |
| robots 상태 | 허용/차단/부분 차단 |
| sitemap 상태 | 포함/누락/오래된 URL |
| 응답 코드 | 200/301/404/403/5xx |
| 내부 링크 | 허브/카테고리/관련 글에서 연결되는가 |
| 수정 액션 | 허용 규칙/사이트맵/리다이렉트/내부 링크 보강 |

## 제출 템플릿

```text
핵심 URL 20개 / robots 상태 / sitemap 포함 여부 / 응답 코드 / 내부 링크 경로 / GEO 영향 / 수정 액션 / 재점검일
```

## 작성 예시

| 입력 항목 | 작성 예시 |
|---|---|
| 핵심 URL | /ko/blog/how-to-get-cited-by-ai |
| robots 상태 | 허용 |
| sitemap 상태 | 포함 |
| 응답 코드 | 200 |
| 내부 링크 | 05장 source/citation 관련 페이지와 블로그 허브에서 연결 |
| 수정 액션 | 관련 glossary와 llms.txt에도 핵심 가이드로 추가 |

## 완료 기준

- 질문셋별 핵심 URL 20개를 골랐습니다.
- robots/sitemap/응답 코드/내부 링크를 따로 기록했습니다.
- 차단 여부만이 아니라 GEO 영향까지 적었습니다.
- 재점검 날짜와 담당자가 있습니다.

## 참고 링크 패키지

이 실습은 HaloX의 [온페이지 SEO 체크리스트](https://haloxlabs.ai/ko/blog/on-page-seo-checklist-2026), [llms.txt 완전 가이드](https://haloxlabs.ai/ko/blog/llms-txt-setup-guide)를 함께 보면 좋습니다.

## 다음 흐름

AI crawler 접근성을 점검했다면 다음은 [06-05. Schema와 내부 링크는 AI 이해를 어떻게 돕나](https://wikidocs.net/346394)에서 페이지 의미와 관계를 더 분명하게 만드는 단계입니다.
