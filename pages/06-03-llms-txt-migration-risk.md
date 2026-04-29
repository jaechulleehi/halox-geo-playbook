## llms.txt와 사이트 이전 리스크 관리

llms.txt는 AI 시스템에 중요한 문서 경로를 안내하는 보조 파일입니다. 하지만 사이트 이전, redirect, canonical, sitemap 문제가 정리되지 않으면 llms.txt만으로는 GEO가 해결되지 않습니다.

사이트 개편과 URL 변경은 기존 source/citation을 흔들 수 있습니다. 기술 변경 전후로 같은 질문셋을 다시 측정해야 합니다. 특히 블로그, 글로서리, 뉴스룸, 제품 문서, 캠페인 랜딩 페이지처럼 AI 답변의 근거가 되는 URL은 이전 계획에 반드시 포함해야 합니다.

## llms.txt는 무엇을 해결하고 무엇을 해결하지 못하나

| 항목 | llms.txt가 돕는 것 | 별도로 점검할 것 |
|---|---|---|
| 핵심 문서 안내 | AI가 우선 읽을 문서 목록을 제시 | sitemap, 내부 링크, robots 접근성 |
| 주제별 허브 | 제품/용어/가이드 경로를 묶음 | 실제 페이지의 본문 품질과 schema |
| 사이트 이전 | 새 핵심 URL 목록을 안내 | 301 redirect, canonical, 구 URL 정리 |
| 콘텐츠 우선순위 | 중요한 글을 선별 | 얇은 페이지/중복 페이지 제거 |

## 사이트 이전에서 자주 생기는 문제

| 문제 | GEO 리스크 | 대응 |
|---|---|---|
| 구 URL이 404로 떨어짐 | 기존 citation/source가 끊김 | 301 redirect와 새 URL 매핑 |
| canonical이 구 URL을 가리킴 | 대표 URL 혼선 | canonical 일괄 검수 |
| sitemap이 늦게 갱신됨 | 새 문서 발견 지연 | 배포 직후 sitemap 재생성 |
| llms.txt가 과거 경로를 유지 | AI 안내 경로 오류 | 핵심 문서 20개부터 재정리 |
| 내부 링크가 구 구조에 남음 | crawler 탐색 흐름 약화 | 허브/관련 글 링크 보정 |

## 사례로 이해하기

캠페인 URL 인용 추적 사례에서는 URL이 짧은 기간에 만들어지고 사라집니다. 캠페인 종료 뒤 랜딩 페이지를 닫아버리면 AI 답변에 남아 있던 citation이 깨질 수 있습니다. 종료 후에도 요약/결과/공식 안내 페이지로 redirect해야 source 안정성을 유지할 수 있습니다.

GEO 지식 베이스를 개편하는 사례에서는 글로서리와 블로그 URL 구조가 바뀌기 쉽습니다. 이때 llms.txt에는 새 경로만 넣고, sitemap과 canonical, 내부 링크에는 구 경로가 남아 있으면 AI가 어느 URL을 신뢰해야 할지 헷갈립니다.

## HaloX 기능으로 설명하는 법

| 기능 흐름 | 설명 방식 |
|---|---|
| Before/after measurement | 사이트 이전 전후 같은 질문셋을 비교한다 |
| Citation URL tracking | 구 URL과 신 URL 중 무엇이 citation 되는지 본다 |
| Source stability | 이전 뒤 source가 흔들리는 질문군을 찾는다 |
| Technical action report | redirect/canonical/sitemap/llms.txt 수정 항목을 나눈다 |

## 실습 워크시트

| 입력 항목 | 작성 기준 |
|---|---|
| 변경 항목 | 도메인/URL/문서 구조/언어/캠페인 종료 |
| AI 접근 파일 | robots/sitemap/llms.txt |
| 리다이렉트 | 301/302/누락/체인 발생 |
| canonical | 새 대표 URL로 정리됐는가 |
| 리스크 | 오래된 출처/중복/누락/깨진 citation |
| 대응 | 수정/모니터링/재측정 |

## 제출 템플릿

```text
이전 전 URL / 이전 후 URL / redirect 상태 / canonical 상태 / sitemap 반영 / llms.txt 반영 / 핵심 페이지 10개 / 재측정 질문
```

## 작성 예시

예시는 `llms.txt와 사이트 이전 리스크 관리`를 가상의 사이트에 적용한 것입니다. 실제 점검에서는 URL, 증상, 개발 담당자, 수정 우선순위를 함께 남깁니다.

| 입력 항목 | 작성 예시 |
|---|---|
| 변경 항목 | 블로그 URL 구조 변경 |
| AI 접근 파일 | sitemap은 갱신, llms.txt는 미반영 |
| 리다이렉트 | 구 URL에서 신 URL로 301 처리 |
| canonical | 일부 글이 구 URL canonical을 유지 |
| 리스크 | AI 답변이 오래된 URL을 citation으로 남길 수 있음 |
| 대응 | 핵심 GEO 글 10개를 llms.txt와 내부 링크 허브에 다시 반영한다 |

## 완료 기준

- 이전 전/후 URL 매핑이 있습니다.
- redirect, canonical, sitemap, llms.txt를 따로 점검했습니다.
- 기존 source/citation이 흔들릴 질문셋을 정했습니다.
- 수정 후 재측정 날짜가 있습니다.

## 참고 링크 패키지

이 실습은 HaloX의 [llms.txt 완전 가이드](https://haloxlabs.ai/ko/blog/llms-txt-setup-guide), [사이트 이전 SEO 체크리스트](https://haloxlabs.ai/ko/blog/website-migration-seo-checklist)를 함께 보면 좋습니다.

## 흔한 질문

**Q. llms.txt만 만들면 AI가 우리 콘텐츠를 잘 읽나요?**

아닙니다. llms.txt는 안내판입니다. robots, sitemap, canonical, 내부 링크, 본문 구조가 같이 정리되어야 합니다.

**Q. 사이트 이전 뒤 언제 재측정해야 하나요?**

배포 직후 기술 오류를 먼저 잡고, 7일/30일 단위로 같은 질문셋을 다시 측정합니다. AI 답변은 즉시 바뀌지 않을 수 있으므로 URL 안정성을 먼저 확인합니다.

## 다음 흐름

이전: [06-02. CSR/SSR 렌더링은 GEO에서 왜 중요한가](https://wikidocs.net/346354) / 다음: [06-04. AI crawler 접근성과 robots/sitemap은 어떻게 점검할까](https://wikidocs.net/346393)
