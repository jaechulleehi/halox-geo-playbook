## 02장 콘텐츠 깊이 보강 감사 메모

## 결론

02장은 `AI 검색 모니터링`을 점수표가 아니라 의사결정 언어로 바꾸는 장이다. 현재 방향은 맞지만, 더 깊게 보강하려면 단순 mention/source/citation 정의를 넘어서 `질문셋 → 플랫폼 → 답변 상태 → 원인 → 담당 액션 → 재측정` 흐름을 명확히 해야 한다.

## 페이지별 보강 기준

| 페이지 | 맡을 역할 | 보강한 방향 |
|---|---|---|
| `02-chapter-2.md` | 01장에서 만든 질문셋을 측정 언어로 바꾸는 parent | 지표 분해 모델과 실행 판단 흐름 추가 |
| `02-01` | ChatGPT 브랜드 노출 진단 | 단순 언급 여부가 아니라 답변 상태/추천 문맥/오류 유형/다음 액션으로 확장 |
| `02-02` | Perplexity/Google AI Overviews 차이 | 플랫폼별 화면 구조, citation 해석, 공식 Google AI features 근거 연결 |
| `02-03` | mention/source/citation 구분 | 세 지표의 조합별 원인/액션과 업종별 해석 추가 |
| `02-04` | AI 검색 리포트 읽기 | 리포트 첫 페이지/월간 회의/30일 액션/대행사 검토 기준 강화 |

## 반영한 근거/소스

| 소스 | 반영 지점 |
|---|---|
| `SOURCE_MAP.md`의 mention/source/citation 성과 프레임 | 02 parent/02-03/02-04 |
| `SOURCE_MAP.md`의 질문 기반 AI 설명 품질 진단 | 02-01/02-04 |
| `BACKLINK_MAP.md`의 02장 링크 전략 | AVI 점수/제품 분석 흐름 연결 |
| `SEO_GEO.md`의 02장 키워드 클러스터 | ChatGPT 브랜드 노출, Perplexity SEO, Google AI Overviews 최적화, 브랜드 언급률, AI 검색 리포트 자연 반영 |
| Google AI features 공식 문서 | 02-02에서 Google AI 기능과 사이트 콘텐츠 포함 기준 참고 링크로 반영 |
| Google Search Console 성과 보고서 | 02 parent/02-04에서 기존 SEO 지표와 GEO 지표를 같이 읽는 근거로 반영 |
| Google Helpful Content 문서 | 콘텐츠/출처 액션이 독자 문제 해결로 이어져야 한다는 기준으로 반영 |

## 다음 보강 후보

- 03장에서는 02장의 약한 질문군을 fan-out으로 확장하는 구조를 더 깊게 잡아야 한다.
- 05장 source/citation 심화 페이지와 02-03이 반복되지 않게, 02장은 리포트 해석/운영 액션 중심으로 유지한다.
- 09장 도구/대행사 검토와 연결되는 `리포트 검증 질문`은 02-04에 짧게 두고, 상세 scorecard는 09장에 남긴다.
