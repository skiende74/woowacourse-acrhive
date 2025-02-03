# woowacourse-archive

우아한테크코스 6기 FE 활동 기록 저장소

활동 기간 : 📅 2024.02.13 - 2024.11.29

## 레벨 1 ( JS 미션 )

📅 2024.02.13 ~ 2024.04.05

### **학습 목표**

- 작은 규모의 어플리케이션들을 만들어보면서 JavaScript/TypeScript 언어의 주요 문법들을 깊이 있게 학습한다.
- 유지보수하기 좋은 코드의 필요성을 경험하고, 어떻게 하면 유지보수하기 좋은 코드를 작성할 수 있을지 고민하고 적용해본다.
- E2E 테스트와 단위 테스트 코드를 작성해보고, 이를 기반으로 리팩터링하며 테스트 코드의 필요성을 경험해본다.
- 주어진 디자인을 웹 표준을 준수하는 UI로 구현해보고, 프론트엔드 개발자로서 고려해야 할 UX에 대해 고민해본다.

### 미션

| **미션**        | **PR**                                                                    | **페어**                                 | **리뷰어**                                |
| --------------- | ------------------------------------------------------------------------- | ---------------------------------------- | ----------------------------------------- |
| 🚗 자동차 경주  | [step 1](https://github.com/woowacourse/javascript-racingcar/pull/284)    | [에프이](https://github.com/chysis)       | [브콜](https://github.com/Tanney-102)     |
|                 | [step 2](https://github.com/woowacourse/javascript-racingcar/pull/322)    | -                                      | [브콜](https://github.com/Tanney-102)     |
| 🎟️ 로또         | [step 1](https://github.com/woowacourse/javascript-lotto/pull/277)        | [시모](https://github.com/simorimi)   | [케빈](https://github.com/JeongBin0227) |
|                 | [step 2](https://github.com/woowacourse/javascript-lotto/pull/319)        | -                                        | [케빈](https://github.com/JeongBin0227) |
| 🍣 점심 뭐 먹지 | [step 1](https://github.com/woowacourse/javascript-lunch/pull/140)        | [리안](https://github.com/ooherin)      | [호프](https://github.com/moonheekim0118)     |
|                 | [step 2](https://github.com/woowacourse/javascript-lunch/pull/177)        | -                                        | [호프](https://github.com/moonheekim0118)     |
| 🎬 영화 리뷰    | [step 1](https://github.com/woowacourse/javascript-movie-review/pull/138) | [마루](https://github.com/rbgksqkr) | [하루](https://github.com/365kim)       |
|                 | [step 2](https://github.com/woowacourse/javascript-movie-review/pull/177) | -                                        | [하루](https://github.com/365kim)       |

### 배운 점
#### 자동차 경주
MVP 구조를 이용해 구현하였습니다. 팀원과 페어 프로그래밍을 하며 페어프로그래밍의 장단점에대해 생각해볼 수 있었습니다.

#### 로또
<details><summary>펼치기</summary>

**TDD** : TDD 수행시 우선테스트를먼저작성하고(레드), 그다음 구현을 하는(그린), **레드-그린 테스트** 과정을 철저히 따르며 구현하였습니다.
놓치는 요구사항 없이 안정감있고 TDD로도 속도감 있는 개발을 할 수 있다고 느꼈습니다.
TDD를 적용할지말지에 대한 기준도 마련할 수 있었는데, 해당문제가 자신에게 익숙한 상황이라면 TDD가 가능하고, 완전히 처음짜보는 문제에서는 TDD가 적절하지 않을 수 있다고 판단했습니다.

**MVP** : MVP구조로, View를 모르는 모델을 만들고, View를 두개(CLI, HTML) 만들어서 하나의 서비스를 수정없이 두가지 뷰에서 사용할 수 있도록 구현하였습니다.


**custom elements** : 스텝2에서 HTML상황에서의 컴포넌트 분리 위해, 웹 컴포넌트 API인 custom elements를 도입하였습니다. 

</details>

- 키워드 : TDD, 인자전달시 POJO(퓨어 JS 객체) 사용, 원시값 래핑, 일급 컬렉션 등
- 읽은 책 : 테스트 주도개발 시작하기(최범균 저)

#### 점심 뭐 먹지
<details><summary>펼치기</summary>

**innerHTML시 XSS 문제 대처** : DB에서 내려온 데이터를 이용하여 innerHTML로 보여주게 될 경우 XSS에 취약하다는 문제가 있었습니다.
따라서 innerHTML에는 DB데이터가 포함되지않은 정적인 데이터만 초기에 띄우고, DB데이터는 querySelector().innerText를 이용하여 띄워줌으로서 
XSS문제를 해결하였습니다.

**is attribute** : 커스텀 elements간에 서로를 재사용하기위해 is attribute를 활용하였습니다.
</details>

- 키워드 : e2e, XSS, custom elements

## 레벨 2

📅 2024.04.16 ~ 2024.06.14

### **학습 목표**

- 레벨1보다 복잡한 규모의 어플리케이션을 React와 TypeScript를 이용해 만들어본다.
- 스토리북을 통하여, 컴포넌트 단위로 피드백을 받기 위한 테스트의 필요성을 경험해본다.
- 유지보수하기 좋은 코드의 필요성을 경험하고, 어떻게 하면 유지보수하기 좋은 코드를 작성할 수 있을지 고민하고 적용해본다.
- 주어진 디자인을 웹 표준을 준수하는 UI로 구현해보고, 프론트엔드 개발자로서 고려해야 할 UX에 대해 고민해본다.

### 미션

| **미션**     | **PR**                                                                   | **페어**                              | **리뷰어**                                |
| ------------ | ------------------------------------------------------------------------ | ------------------------------------- | ----------------------------------------- |
| 💳 페이먼츠  | [step 1](https://github.com/woowacourse/react-payments/pull/361)         | [리안](https://github.com/ooherin) | [지그](https://github.com/zigsong)       |
|              | [step 2](https://github.com/woowacourse/react-payments/pull/406)         | -                                     | [지그](https://github.com/zigsong)       |
| 🧩 모듈      | [step 1](https://github.com/woowacourse/react-modules/pull/38)           | [월하](https://github.com/vi-wolhwa)     | [블링](https://github.com/uk960214) |
|              | [step 2](https://github.com/woowacourse/react-modules/pull/56)           | -                                     | [블링](https://github.com/uk960214) |
| 🛒 장바구니  | [step 1](https://github.com/woowacourse/react-shopping-cart/pull/275)    | [텐텐](https://github.com/chlwlstlf)     | [브콜](https://github.com/Tanney-102)   |
|              | [step 2](https://github.com/woowacourse/react-shopping-cart/pull/323)    | -                                     | [브콜](https://github.com/Tanney-102)   |
| 🧺 상품 목록 | [step 1](https://github.com/woowacourse/react-shopping-products/pull/21) | [프룬](https://github.com/chosim-dvlpr)   | [케빈](https://github.com/JeongBin0227)         |
|              | [step 2](https://github.com/woowacourse/react-shopping-products/pull/71) | -                                     | [케빈](https://github.com/JeongBin0227)         |


## 레벨 3 ~ 4. 팀 프로젝트 - 모바일 웹 방끗(bang-ggood)

활동 기간 : 📅 2024. 07. 02 ~ 2024.11.31 (5개월)

#### [방끗 서비스 바로가기](https://bang-ggood.com/)
#### [방끗 Repository 바로가기](https://github.com/woowacourse-teams/2024-bang-ggood)

서비스 기획부터, AWS 배포 및 CI/CD 자동화, 운영까지의 전체 사이클을 애자일한 방법으로(2주단위 스프린트 x 8회) 경험해볼 수 있었습니다.
팀 구성 : FE: 3명 BE: 4명

<table>
    <td><a href="https://github.com/woowacourse-teams/2024-bang-ggood">방끗 깃허브</a></td>
    <td><a href="https://bang-ggood.com/">방끗 페이지</a></td>
    <td><a href="https://github.com/woowacourse-teams/2024-bang-ggood/wiki">방끗 wiki</a></td>
    <td><a href="https://www.figma.com/board/nAlskmwHcmlvbhiT1L1cSK/%EB%B0%A9%EB%81%97-%ED%94%BC%EA%B7%B8%EC%9E%BC?node-id=0-1&t=XAdJbckT6RXSdRsY-1">방끗 회의 Figjam</a></td>
</table>



## 레벨 3 미션

📅  2024.07.02 ~ 2024.09.02

### **학습 목표**

#### **함께** 서비스를 **개발**하고 **운영**하는 경험

- 함께
  - 팀으로 협업하는 경험
- 개발
  - 개발 프로세스를 기반으로 프로젝트를 진행하는 경험
  - 하나의 서비스를 실제 사용자가 쓸 수 있도록 개발하고 배포하는 경험
  - ‘문제를 해결하기 위한’ 기술 학습 및 적용
- 운영
  - 실 사용자가 있는 서비스를 유지보수하는 경험

## 레벨 4 미션

📅  2024.09.03 ~ 2024.11.01

### **학습 목표**

- 성능: 서비스의 성능 개선이 필요할 때, 직접 문제를 정의하고 정의한 문제에 맞는 해결책을 도입할 수 있다.
- 웹 접근성: 서비스의 접근성 개선이 필요할 때, 직접 문제를 정의하고 정의한 문제에 맞는 해결책을 도입할 수 있다.
- 서버 사이드 렌더링: CSR과 SSR 렌더링 방식의 특징을 이해하고, 주어진 상황에 적합한 렌더링 방식을 선택할 수 있다. 또한, 이를 리액트 앱과 함께 적용할 수 있다.

### 미션

| **미션**                        | **PR**                                                        | **리뷰어**                                | 리뷰이                                |
| ------------------------------- | ------------------------------------------------------------- | ----------------------------------------- | ------------------------------------- |
| 🛠️ 웹 성능 개인 미션            | [PR 링크](https://github.com/woowacourse/perf-basecamp/pull/134) | [파란](https://github.com/greetings1012) | [바다](https://github.com/BadaHertz52) |
| 👨‍👩‍👧‍👦 웹 접근성 개인 미션          | [PR 링크](https://github.com/woowacourse/a11y-airline/pull/111)  | [버건디](https://github.com/brgndy)      | [월하](https://github.com/vi-wolhwa)    |
| 💻 서버 사이드 렌더링 개인 미션 | [step 1](https://github.com/woowacourse/react-ssr/pull/32)    | [에프이](https://github.com/chysis)     | [소하](https://github.com/soi-ha)     |
|                                 | [step 2](https://github.com/woowacourse/react-ssr/pull/60)    | [에프이](https://github.com/chysis)     | [소하](https://github.com/soi-ha)     |

## 글쓰기

### 테크니컬 라이팅

[startTransition, useDeferredValue 활용한 React 동시성 렌더링](https://github.com/skiende74/woowa-writing/blob/main/%ED%85%8C%ED%81%AC%EB%8B%88%EC%BB%AC%EB%9D%BC%EC%9D%B4%ED%8C%85_%EB%8F%99%EC%8B%9C%EC%84%B1%EB%A0%8C%EB%8D%94%EB%A7%81.md)


React 18의 기능이지만 깊게 이해하지 못해 그동안 잘 활용하지 못하고 있다고 생각했습니다.
공식문서는 startTransition과, useTransition, useDeferredValue 각각은 잘 설명하지만, 
셋 모두 유사한 기능인데도 셋 다 전부 다른 예제를 사용하고있어 구체적인 차이점을 이해하기 어렵다고 판단했습니다.
따라서 하나의 예제에서 셋을 모두 다루면서 구체적으로 어떤 차이점을 갖는지, 어떤 상황에서 뭘 써야할지에 대한 기준을 제시하고자했습니다.
그래서 동시성렌더링의 필요성과, 각각의 차이점을 정리하는 것을 주제로 작성해보았습니다.


## 테코톡 발표

[[10분 테코톡] 제이드의 Webpack](https://www.youtube.com/watch?v=-m9xGyePEug)

프로젝트 작업시 Webpack의 대략적인 동작은 이해하고 있었으나, 각 설정의 의미나 동작과정을 상세하게 이해하지못하고있다고 생각했습니다. 그래서 웹팩에 대해 정확하게 이해하고자 테코톡을 신청하여 발표하였습니다. 또한 동료들의 웹팩 프로젝트 초기설정에 도움을 주고자하였습니다.
