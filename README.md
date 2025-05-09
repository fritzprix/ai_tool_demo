---
marp: true
headingDivider: 2
---

<!--class: invert -->

# AI Tool 101

> David Lee @ AI성장전략본부

## Table of Content

![bg right fit](res/audience.png)

- Basic
  - Deep Research
  - 범용 Web AI Agent
  - NotebookLM
- Advanced
  - Canvas (Artifact) - PPT활용
  - Deeper Research - 프롬프트 증강
- (선택) Cursor 활용 문서 작성

## Deep Research (1)

- Web 검색을 활용 정보의 Retrieval과 자율적 계획과 추론에 따라 주제에 대한 연구를 수행
- Grok 무료 옵션 (Rate Limit) / Perplexity Pro
- [Sample](./demo/us_tariff/o3-mini-high.md)

![bg right fit](./res/deepr_2x.gif)

## Deep Research (2) - 예시

- "Trump 정부 관세 정책의 Global 경제 영향 심층 분석"에 대한 결과

  > Gemini-2.5 Pro / Grok /</br>o3-mini / Perplexity

- 같은 주제에 상이한 결과
  - Gemini가 가장 상세한 리포트
  - Grok이 가장 간결

![bg right fit](https://mermaid.ink/img/pako:eNpVj01ugzAQha9izdogAzY_XnTTqhfoolJDFTnxFKwARo6RoFHuXgNt1c7Kb-abN343OFuNIGFezq1yPjqhV_VAQnnjOyQ1vFqnyaOdBk9OC3k2HdawE3OkZnMlhwZ7M5hjehRxrylpnL0cNeKI7r_elM2ilY5a07RbI2Bjh7PxS5Dvu_OyO_89XgNhJIoeSMUY26mTcuRQiqqkpEpTSrjIKUlZVlCScM7fgUKPrldGh4C3dacG32IfAsjw1Mpd1ij3wKnJ25dlOIP0bkIKzk5NC_JDddegplErj09GNU71v93GrcbfPA4a3fZRkElGYVTDm7X9zzxIkDeYw1CUcZakPBcsz1mVsJLCApKXMc8KXpSMZaLKi-pO4XMzYHFZiJCZpTkrCpaK5P4FD-SFDA?type=png)

## 범용 Web AI Agent

- OpenAI의 Operator가 대표적 (Plus 구독 필요)
- Manus AI 현재 Closed Beta
- Convergence.ai에서 Proxy (무료 ~ $20/월)
  - Memory 지원, Agent가 실패하는 지점에서 사용자가 시연을 통해 지도 가능
  - Orchestrator(대화형 Agent)와 Proxy (특정 역할 수행) 다중 Agent 구조

## Proxy (1)

<style scoped>
ul {
  font-size: 28px;
}
</style>

![bg right fit](./res/proxy_2x.gif)

- 강점
  - `상대적`으로 저렴하고 누구나 접근 가능
  - Template을 통해 작업을 재사용 가능한 형태로 만들고 공유 가능
  - Automation 지원, 주기적으로 해당 Task를 수행, 결과 전송 </br>(메일, 메신저)
- 한계
  - Captcha (Bot Filter)
  - 느린 속도

## Proxy (2)</br>- Automation 활용

- 무료 계정 1개 / 유료 20개 까지

- 예시
  - 스타트업 서치
  - 신규 트렌딩 기술 및 논문 서치
  - ...

![bg fit left](./res/proxy_autp_report.png)

## NotebookLM

- Audio Learner를 위한 선택지
- Google의 NotebookLM (무료)
  > 관심 주제 Deep Research > NotebookLM > 출퇴근 Podcast

<audio controls>
  <source src="./res/nb_lm.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

![bg left fit](./res/np_lm.gif)

## Canvas (Artifact)

- Claude / Gemini / ChatGPT 등 유사한 기능
- 코드 (Javascript)를 실행 시킬 수 있는 환경 (React / WebGL ..)
- 간단한 웹 게임이나 시각화 / 시뮬레이션 등 가능

## Canvas (Artifact) - PPT 활용 하기(1)

<style scoped>
  ul {
    font-size:24px;
  }
</style>

- 시각화 작업 [파일](./demo/us_tariff_augmented/grok_deeper.md) 준비

- 시각화 Prompt

  ```text
  # 시각화 제작 요청

  1. **데이터 분석 및 시각화 (데이터 유형 적응성):**

  - 첨부의 보고서 중 시각화 가능한 요소를 분석하여 추출합니다.
  - 추출된 정보들의 Scale,단위 및 속성에 따라 이상적인 시각화 방식을 선택하여 데이터를 표현합니다.
  - 불필요하거나 시각화에 부적합한 요소는 가급적 제거하고 직관적으로 이해될 수 있도록 합니다.

  1. **디자인 및 품질:**

  - 내부 임원 보고에 적합하도록 깔끔하고 전문적인 디자인을 적용해야 합니다.
  - 표기되는 데이터, 수치, 내용에 오류가 없어야 합니다.

  1. **기술 및 레이아웃:**

  - 슬라이드 비율: 개별 슬라이드는 16:9 가로세로 비율로 제작되어야 합니다.
  - React 사용합니다. 코드에 오류가 없도록 차근차근 코드를 작성합니다.
  - 향후 SVG로 추출 가능성이 있음을 참고하세요.

  ```

  - React : 요소들간의 보다 안정적인 layout을 보장

![bg right fit](res/blank.png)

## Canvas (Artifact) - PPT 활용 하기(1)

<style scoped>
  ul {
    font-size:24px;
  }
</style>

- 시각화 작업 [파일](./demo/us_tariff_augmented/grok_deeper.md) 준비

- 시각화 Prompt

  ```text
  # 시각화 제작 요청

  1. **데이터 분석 및 시각화 (데이터 유형 적응성):**

  - 첨부의 보고서 중 시각화 가능한 요소를 분석하여 추출합니다.
  - 추출된 정보들의 Scale,단위 및 속성에 따라 이상적인 시각화 방식을 선택하여 데이터를 표현합니다.
  - 불필요하거나 시각화에 부적합한 요소는 가급적 제거하고 직관적으로 이해될 수 있도록 합니다.

  1. **디자인 및 품질:**

  - 내부 임원 보고에 적합하도록 깔끔하고 전문적인 디자인을 적용해야 합니다.
  - 표기되는 데이터, 수치, 내용에 오류가 없어야 합니다.

  1. **기술 및 레이아웃:**

  - 슬라이드 비율: 개별 슬라이드는 16:9 가로세로 비율로 제작되어야 합니다.
  - React 사용합니다. 코드에 오류가 없도록 차근차근 코드를 작성합니다.
  - 향후 SVG로 추출 가능성이 있음을 참고하세요.

  ```

  - React : 요소들간의 보다 안정적인 layout을 보장

![bg right fit](res/artifact_demo_prompt_simple_2x.gif)

## Canvas (Artifact) - PPT 활용 하기(1-1)

- 결과 비교

  - [React 결과물](https://claude.site/artifacts/2516439f-e06a-48ad-aebf-cdf522840d00)

- 시각화 결과물의 수정

  - 해당 시각화 스크린샷
  - Image Prompt와 함께 문제점 분석을 지시

    ```text
    시각화에 문제가 있습니다. 이미지를 정밀하게 살펴보고 원인을 차근차근 분석해주세요
    ```

- 이미지 스샷 vs SVG 추출

## Canvas (Artifact) - PPT 활용 하기(2)

- 결과물의 레이아웃 등이 만족스럽지 않거나 PPT에 넣어 직접 수정을 원할 경우
- SVG로 변환하기

  ```prompt
  위 시각화를 각각 SVG로 만들어주세요.
  ```

- [SVG 결과물 - 1](https://claude.site/artifacts/ae55aee0-80d0-4cfb-93e1-8c25bd837643)
- [SVG 결과물 - 2](https://claude.site/artifacts/529adc1a-a54e-4b63-879c-c5a3cf57b5eb)

![bg right fit](res/claude_slide_3_2x.gif)

## Canvas (Artifact) - PPT 활용 하기(3)

- SVG 다운로드 PPT에 삽입
- 그룹 해제 후 편집 가능

![bg right fit](res/claude_slide_4_2x.gif)

## Canvas (Artifact) - 기타

- [복잡한 개념 이해 (애니메이션)](https://claude.site/artifacts/b2cd28f2-8520-457f-9641-5b032f3d6d7e)
- [토큰 비용 시뮬레이션](https://claude.site/artifacts/215fdcb0-ba18-4c74-9676-a063443aa046)

![bg right fit](./res/ring_attention_1x_noskip.gif)

## Deeper Research </br>- Query Augmentation (1)

<style scoped>
p {
   font-size:16px;
}
</style>

- Deep Research가 포인트를 제대로 잡지 못할 때
- Prompt 증강 기법을 활용
  - AI를 활용 Research Firm의뢰를 위한 Guide 생성
    > 트럼프 관세 정책이 Global 경제에 미칠 영향이라는 주제로 심층 연구를 Research Firm에 의뢰하려고 합니다. 심도있고 포괄적인 연구가되도록 상세한 요청서를 작성해주세요
  - 증강된 Prompt 활용 Deep Research 수행

![bg right fit](res/dapdap.png)

## Deeper Research </br>- Query Augmentation (2)

```text
# 트럼프 관세 정책의 글로벌 경제 영향 연구 의뢰서

## 연구 배경 및 목적

도널드 트럼프 대통령의 재선으로 인해 새로운 관세 정책이 예상되는 상황에서, 이러한 정책이 글로벌 경제와 시장에 미칠 잠재적 영향에 대한 포괄적인 이해가 필요합니다. 
본 연구는 트럼프 행정부의 관세 정책을 분석하고, 이에 대한 글로벌 경제의 반응과 장단기적 영향을 평가하는 것을 목적으로 합니다.

## 연구 범위

### 1. 정책 분석
- 트럼프 행정부의 기존 관세 정책(2017-2021) 검토 및 평가
- 현재 제안된 새로운 관세 정책의 세부 내용 분석
- 관세 정책 시행의 법적, 제도적 메커니즘 분석
- 주요 목표 대상국가(중국, EU, 멕시코, 캐나다 등) 및 산업 분석

### 2. 경제적 영향 평가
- 글로벌 무역 흐름과 패턴 변화 예측
- 주요 산업별 영향 분석(자동차, 전자, 철강, 농업 등)
- 글로벌 공급망 재편 가능성 및 영향
- 인플레이션, 물가, 고용 등 거시경제 지표에 미치는 영향
- 주요 국가별 GDP 성장률 및 경제지표 영향 전망


### 3. 금융 시장 영향
- 주식, 채권, 외환 시장 반응 예측
- 금융 안정성에 대한 잠재적 위험 평가
- 투자 흐름 변화 및 FDI(외국인직접투자) 패턴 분석

### 4. 정책 대응 시나리오
- 주요 무역 상대국들의 잠재적 대응 조치 분석
- 다양한 관세 시나리오에 따른 경제적 결과 시뮬레이션
- 상호 보복 관세의 잠재적 에스컬레이션 경로 및 영향

### 5. 산업별 및 지역별 세부 분석
- 한국 경제에 미치는 특별 영향 분석
- 아시아, 유럽, 북미, 남미 지역별 차별화된 영향
- 산업별 취약성 및 기회 평가

## 연구 방법론

1. **정량적 분석**
   - 계량경제학적 모델링 및 시뮬레이션
   - 무역 데이터 및 경제지표 기반 통계 분석
   - 산업연관분석을 통한 파급효과 추정

2. **정성적 분석**
   - 정책 전문가, 경제학자, 산업 리더 인터뷰
   - 과거 유사 정책 사례 분석
   - 기업 및 정부 반응 패턴 분석

3. **시나리오 분석**
   - 주요 변수에 따른 다중 시나리오 개발
   - 최악/최선/가능성 높은 시나리오별 영향 평가
   - 시간대별 경제 영향 변화 추적(단기/중기/장기)

## 기대 산출물

1. **종합 보고서**
   - 주요 연구 결과 및 정책 함의를 담은 포괄적 분석 보고서
   - 데이터 기반 인사이트 및 전략적 시사점 제공

2. **시각화 자료**
   - 핵심 데이터 및 예측 결과를 보여주는 대시보드
   - 정책-영향 관계 시각화 자료
   - 산업 및 지역별 영향 히트맵

3. **정책 브리핑**
   - 주요 이해관계자를 위한 요약 보고서
   - 정책 결정자 및 기업 전략가를 위한 실행 가능한 인사이트

4. **분기별 업데이트**
   - 정책 변화 및 실제 경제 영향에 따른 분기별 업데이트 보고서
   - 예측과 실제 결과 비교 분석

```

![bg right fit](./res/promt_aug_comp.png)

## Cursor (+Markdown)

- **Vibe Working**을 추구하는 구성원
- Learning Curve 존재

### Why

- 다수의 파일을 AI에 Feed/재사용 용이
- 다양한 서식 지원
  - Markdown / Mermaid / Marp ...
- MCP를 통한 다양한 툴 활용
- 반복 업무의 Program화 `AI 코딩 활용` / Template화

![bg right fit](./res/vibe_working.png)

## Markdown

- 간략한 서식을 지원
- LLM 학습 시 코드 데이터 중 많은 부분 차지
- 따라서 AI가 잘 이해하고 (구조)
- Prompting 활용하기 용이

![bg fit right](res/markdown_example.png)

## Cursor Demo</br>- Trump 관세 영향 보고서 평가하기 (1)

- 아래 Prompt로 [평가 Guide](./demo/eval/eval_guide.md)를 생성

  ```markdown
  연구 보고서의 품질을 평가하기 위한 Guide 제안
  ```

- 해당 Guide를 입력으로 평가 [Template](./demo/eval/eval_template.md)을 생성 (Cursor)

![bg right fit](./res/eval_template.png)

## Cursor Demo</br>- Trump 관세 영향 보고서 평가하기 (2)

- Template을 활용 평가하여 결과를 저장하도록 명령

![bg right fit](./res/cursor_prompt.png)

## Cursor Demo</br>- 보고서 평가하기 (3)

- Agent의 임무 실행 지켜보기
- 하지만.. 한번에 성공하지 않을 수 있음, 재시도의 용이성이 핵심

![bg right fit](./res/cursor_vibe_1x_noskip.gif)

## Cursor Demo</br>- 보고서 평가 (4)

- (Coding) 결과를 CSV로 추출하기 위한 프로그램 만들기
- (Coding) 추출된 CSV를 시각화 하기 위한 프로그램 만들기

![bg right fit](./res/conversion_work_1x.gif)

## Cursor Demo</br>- 보고서 평가 (5)

> 총 10개 DeepSearch 자료에 대한 주요한 Insight를 10분내 추출, 시각화

![bg right fit](./res/eval_result.png)

## Cursor Live Demo</br>- 보고서 취합 (6)

> 전체 보고서를 하나의 구조화된 보고서로 만들기

## Wrap-Up

<style scoped>
ul {
  font-size: 28px;
}
p {
  font-size: 26px;
}
</style>

- 시각의 전환 필요 (Programming => 자연어)

  > 나는 못해. 개발자나 쓰는거야..

- 창의적 게으름

  > 새로운 AI 적용 가능성을 발견

- Hallucination
  > 최종 확인에서 사람의 역할 중요

> 금일 세션 자료 모두 [Github에 공개](https://github.com/dropthekeyboard/ai_tool_demo)

![bg right fit](res/andrej_english.png)

## Thank You

## Appendix - Augmented Query

```text
# 트럼프 관세 정책의 글로벌 경제 영향 연구 의뢰서

## 연구 배경 및 목적

도널드 트럼프 대통령의 재선으로 인해 새로운 관세 정책이 예상되는 상황에서, 이러한 정책이 글로벌 경제와 시장에 미칠 잠재적 영향에 대한 포괄적인 이해가 필요합니다. 본 연구는 트럼프 행정부의 관세 정책을 분석하고, 이에 대한 글로벌 경제의 반응과 장단기적 영향을 평가하는 것을 목적으로 합니다.

## 연구 범위

### 1. 정책 분석
- 트럼프 행정부의 기존 관세 정책(2017-2021) 검토 및 평가
- 현재 제안된 새로운 관세 정책의 세부 내용 분석
- 관세 정책 시행의 법적, 제도적 메커니즘 분석
- 주요 목표 대상국가(중국, EU, 멕시코, 캐나다 등) 및 산업 분석

### 2. 경제적 영향 평가
- 글로벌 무역 흐름과 패턴 변화 예측
- 주요 산업별 영향 분석(자동차, 전자, 철강, 농업 등)
- 글로벌 공급망 재편 가능성 및 영향
- 인플레이션, 물가, 고용 등 거시경제 지표에 미치는 영향
- 주요 국가별 GDP 성장률 및 경제지표 영향 전망

### 3. 금융 시장 영향
- 주식, 채권, 외환 시장 반응 예측
- 금융 안정성에 대한 잠재적 위험 평가
- 투자 흐름 변화 및 FDI(외국인직접투자) 패턴 분석

### 4. 정책 대응 시나리오
- 주요 무역 상대국들의 잠재적 대응 조치 분석
- 다양한 관세 시나리오에 따른 경제적 결과 시뮬레이션
- 상호 보복 관세의 잠재적 에스컬레이션 경로 및 영향

### 5. 산업별 및 지역별 세부 분석
- 한국 경제에 미치는 특별 영향 분석
- 아시아, 유럽, 북미, 남미 지역별 차별화된 영향
- 산업별 취약성 및 기회 평가

## 연구 방법론

1. **정량적 분석**
   - 계량경제학적 모델링 및 시뮬레이션
   - 무역 데이터 및 경제지표 기반 통계 분석
   - 산업연관분석을 통한 파급효과 추정

2. **정성적 분석**
   - 정책 전문가, 경제학자, 산업 리더 인터뷰
   - 과거 유사 정책 사례 분석
   - 기업 및 정부 반응 패턴 분석

3. **시나리오 분석**
   - 주요 변수에 따른 다중 시나리오 개발
   - 최악/최선/가능성 높은 시나리오별 영향 평가
   - 시간대별 경제 영향 변화 추적(단기/중기/장기)

## 기대 산출물

1. **종합 보고서**
   - 주요 연구 결과 및 정책 함의를 담은 포괄적 분석 보고서
   - 데이터 기반 인사이트 및 전략적 시사점 제공

2. **시각화 자료**
   - 핵심 데이터 및 예측 결과를 보여주는 대시보드
   - 정책-영향 관계 시각화 자료
   - 산업 및 지역별 영향 히트맵

3. **정책 브리핑**
   - 주요 이해관계자를 위한 요약 보고서
   - 정책 결정자 및 기업 전략가를 위한 실행 가능한 인사이트

4. **분기별 업데이트**
   - 정책 변화 및 실제 경제 영향에 따른 분기별 업데이트 보고서
   - 예측과 실제 결과 비교 분석

## 연구 일정

- **1단계**: 초기 정책 분석 및 연구 프레임워크 구축 (4주)
- **2단계**: 경제적 영향 모델링 및 데이터 분석 (8주)
- **3단계**: 시나리오 개발 및 테스트 (6주)
- **4단계**: 최종 보고서 작성 및 결과 시각화 (4주)

## 연구팀 요구사항

- 국제 무역 정책 전문가
- 거시경제 모델링 전문가
- 산업별 분석가(자동차, 전자, 철강, 농업 등)
- 데이터 사이언티스트 및 계량경제학자
- 정책 분석가 및 지정학적 리스크 전문가
- 지역별 전문가(아시아, 유럽, 북미, 남미)

## 기타 요구사항

- 모든 데이터 소스는 투명하게 공개되어야 함
- 분석의 가정과 한계점을 명확히 기술
- 연구 결과의 주기적 업데이트 및 정책 변화에 따른 수정 계획 포함
- 최종 보고서는 한국어와 영어로 제공
- 경영진을 위한 요약 및 기술적 부록 모두 포함

이 연구를 통해 트럼프 관세 정책의 글로벌 경제 영향에 대한 심층적 이해를 바탕으로, 기업과 정부의 전략적 의사결정을 지원하고자 합니다.
```

## Appendix - Claude Artifact 활용 예시

- [프롬프트 시나리오별 가격 시뮬레이션](https://claude.site/artifacts/215fdcb0-ba18-4c74-9676-a063443aa046)
- [DCF Valuation 계산기](https://claude.site/artifacts/de784749-bc58-4bd9-9df9-e229fdac6372)
- [MCP 시각화](https://claude.site/artifacts/baaf6080-bcf2-428c-8598-0cef913156dc)
- [Tetris 게임](https://claude.site/artifacts/d1c53afa-b634-4518-9e98-ea99871a6dea)
