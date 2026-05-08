## CSR/SSR 렌더링과 GEO 크롤링 리스크

![CSR과 SSR 렌더링 리스크](../assets/images/page-heroes/halox-geo-06-02-csr-ssr-rendering-hero.png)

AI와 검색엔진은 사람이 보는 화면과 같은 방식으로 페이지를 읽지 않을 수 있습니다. 브라우저에서는 본문이 잘 보이지만, 초기 HTML에는 핵심 내용이 없고 JavaScript 실행 뒤에야 본문이 나타난다면 crawler가 페이지를 약하게 이해할 수 있습니다.

CSR/SSR 점검의 목적은 특정 프레임워크를 비판하는 것이 아닙니다. AI가 답변 근거로 쓸 핵심 문장, 표, FAQ, schema가 안정적으로 읽히는 위치에 있는지 확인하는 것입니다.

[TOC]

## 사람 화면과 crawler 화면을 나눠 본다

렌더링 문제는 “페이지가 보이냐”가 아니라 “누가 어떤 시점에 무엇을 읽느냐”의 문제입니다.

| 관점 | 확인할 것 | 위험 신호 |
|---|---|---|
| 초기 HTML | 제목, 첫 답변, 핵심 본문 | 빈 div와 script만 있음 |
| 렌더링 후 DOM | 실제 본문, FAQ, 표 | 중요한 문장이 늦게 삽입됨 |
| crawler 접근 | HTTP 상태, robots, 렌더링 가능성 | 봇이 리소스를 못 읽음 |
| citation 후보 | 안정적인 URL과 본문 위치 | 답변 근거 문장이 화면마다 달라짐 |

## HaloX 사이트 진단과 함께 보는 법

사이트 진단의 Pages 탭에서 GEO 점수가 낮은 URL을 먼저 고릅니다. 특히 리포트 예시, 비교 페이지, FAQ, 상품/지점 페이지처럼 citation 후보가 되어야 하는 URL을 우선 확인합니다.

그다음 실제 페이지의 초기 HTML과 렌더링 후 DOM을 비교합니다. 핵심 답변이 초기 HTML에 없거나, 제목/메타는 있는데 본문이 늦게 나타나는 경우 개발팀과 SSR, pre-rendering, hydration 구조를 점검합니다.

인용 추적에서 공식 URL이 계속 빠진다면 렌더링 이슈와 함께 canonical, 내부 링크, schema를 같이 봅니다. 렌더링 문제 하나만 고쳐도 citation이 바로 생긴다고 단정하지 않습니다.

![CSR/SSR 렌더링 점검 흐름](../assets/images/body-figures/halox-geo-06-02-csr-ssr-rendering-visibility.png)

*렌더링 점검은 사람이 보는 화면, 초기 HTML, 렌더링 후 DOM, crawler 접근을 나눠 확인하는 작업이다.*

## 가상 기업 AcmeGEO 예시

AcmeGEO의 비교 페이지는 브라우저에서 잘 보입니다. 하지만 초기 HTML에는 제품명과 가격 비교표가 없고, 모든 내용이 클라이언트 렌더링 뒤에 삽입됩니다. AI 답변은 해당 페이지 대신 외부 리뷰를 citation으로 보여줍니다.

수정은 핵심 첫 답변, 비교표, FAQ를 서버에서 먼저 전달하는 방향으로 잡습니다. 렌더링 개선 뒤 사이트 진단과 같은 질문 세트의 citation 변화를 함께 확인합니다.

## 정리 양식

```text
점검 URL:
초기 HTML에 보이는 핵심 문장:
렌더링 후에만 보이는 요소:
FAQ/표/schema 위치:
공식 URL citation 여부:
수정 방향:
담당자:
재측정 질문:
```

## 다음 흐름

렌더링을 확인한 뒤에는 llms.txt, site migration, canonical 변화처럼 AI와 검색엔진이 URL을 이해하는 방식을 바꾸는 리스크를 봐야 합니다. 이어서 [llms.txt와 GEO 사이트 이전 리스크 관리](https://wikidocs.net/346355)를 읽습니다.
