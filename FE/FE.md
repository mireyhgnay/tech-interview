# FE (Front-End)

<br />

### 최근에 해결한 기술적인 문제는 무엇이였나요?

<details>
  <summary>나의 답변 (👈 Click)</summary>

티몬 메인홈을 크롬 라이트하우스를 통해서 성능 점수를 50점대에서 70점대까지 올린 경험이 있습니다.

초기 렌더링 속도를 3.9 → 1.9초까지 단축시켰습니다.

렌더링 속도를 높이기 위해서 swiper 활성화를 뷰포트에 맞게 제어하고, 불필요한 태그를 제거하는 등 성능 최적화 작업을 진행하였습니다.

</details>

---

<br />

### 노드 버전 관리는 무엇을 사용했나요?

<details>
  <summary>나의 답변 (👈 Click)</summary>

nvm(node version manager)으로 노드 버전 관리했습니다. npm으로 패키지 관리했습니다.

Node.js는 정기적으로 업데이트가 이루어지고, 각 프로젝트마다 요구되는 노드버전이 다를 수 있습니다.

어느 프로젝트에서는 최신 버전을, 다른 프로젝트에서는 이전 버전을 사용하는 경우가 생깁니다.

이럴때 노드 버전 관리를 통해 원하는 버전을 쉽게 전환하고 사용할 수 있습니다.

</details>

---

<br />

### 브랜치 전략은 무엇을 사용했나요?

<details>
  <summary>나의 답변 (👈 Click)</summary>

git-flow 전략을 사용했습니다.

dev, master 브랜치가 존재하고 dev는 개발 서버 관리용으로 사용됩니다.

항상 dev와 master는 동기화하여 내용을 일치시켜 놓았습니다.

dev에서 작업 브랜치를 따서 작업하고  
 release/ : 기본 운영건이나 몇일 더 걸리는 프로젝트는 release 브랜치명을 사용했고  
 feature/ : 공통 전역에 반영되는 작업은 feature 브랜치명 사용,  
 hofix/ : 긴급배포건은 hotfix 명칭을 사용했습니다. master에서 따서 브랜치를 사용하고 그 날 바로 배포하였습니다.

</details>

---

<br />

### 디자인 패턴은?

<details>
  <summary>나의 답변 (👈 Click)</summary>

특정 패턴을 사용하자! 라고 해서 고정된 방법은 없었습니다.  
 프로젝트의 요구 사항에 맞게 상황에 따라 적합한 대응을 해서 작업했었습니다.

예를들어, 찜하기 기능을 서비스 전반적으로 공통으로 사용된다고 했을 때  
 찜하기 기능 전체를 특정 UI기능으로 만들어 놓고 여러 서비스에서 불러와 공통으로 사용할 수 있도록 하였습니다.  
 특정 기능을 모듈화해서 재사용성이 높일 수 있도록 작업할 수 있도록 하였습니다.

**디자인 패턴이란?**
디자인패턴은 설계에서 자주 등장하는 문제를 해결하기 위해서 어떻게 설계할 건지를 결정하는 방법입니다.  
 재사용성, 확장성, 유지보수성 을 높일 수 있습니다.

</details>

---

<br />

### 어떤 프레임워크를 사용하여 개발했나요?

<details>
  <summary>나의 답변 (👈 Click)</summary>
  
  오랜된 서비스들이 많아서 제이쿼리나 자바스크립트도 꽤 많은 편이였고,     
  리액트로도 주로 많이 구현되어 있었습니다.     
  신규로 구현하고자 하는 페이지들은 리액트나 타입스크립트를 사용하려고 했습니다.
</details>

---

<br />

### 왜 그 프레임워크를 사용했나요?

<details>
  <summary>나의 답변 (👈 Click)</summary>

자바스크립트가 불편해서 리액트나 타입스크립트를 선호한 것은 아닙니다.  
 개인적으로는 자바스크립트로 구현하는 것도 편하고 재밌었습니다.  
 리액트가 컴포넌트 모듈화가 가능하니 재사용성이나 유지보수성 쪽에서 좋다고 생각이 들어서
JS코드들을 리액트로 변환하려고 했습니다.  
 특히 JSX문법이 굉장히 편리하다고 생각했습니다.

</details>

---

<br />

### RESTful API 에 대해서 설명해주세요.

<details>
  <summary>나의 답변 (👈 Click)</summary>

**REST API는 HTTP프로토콜을 기반으로 자원을 CRUD 방식을 사용해서 처리하는 웹서비스 인터페이스입니다.**

- HTTP프로토콜 : 웹에서 서버와 클라이언트 간 데이터를 주고받기 위한 통신 규약
- 자원 : HTTP URI
  - ex. [https://www.example.com:443/path/to/resource?query=example#section1](https://www.example.com/path/to/resource?query=example#section1)
    - 스킴(Scheme): `https`
    - 호스트(Host): `www.example.com`
    - 포트 번호(Port): `443`
    - 경로(Path): `/path/to/resource`
    - 쿼리 문자열(Query String): `?query=example`
    - 프래그먼트(Fragment): `#section1`
- CRUD를 사용해서 서버와 클라이언트 간 통신을 가능하게 합니다.

---

**그렇다면 RESTful API 란?**
RESTful 은 REST 설계 규칙을 올바르게 사용한 API를 말합니다.
설계규칙을 잘 지켜야만 **RESTful**하다. 라고 말할 수 있습니다.

- HTTP 메소드를 사용해서 서버와 통신합니다. (GET, POST, PUT, DELETE)
- URI 방식을 제대로 작성해야 합니다.
- CRUD 기능을 모두 POST로만 처리하는 API는 RESTful하지 못한 것 입니다.

</details>

---

<br />

### 그렇다면 HTTP 메소드에 대한 설명도 해주세요.

<details>
  <summary>나의 답변 (👈 Click)</summary>

- GET : 서버에서 데이터를 요청하는 메소드, 요청한 데이터를 처리해서 응답
- POST : 서버에 데이터를 전송하는 메소드, 전송해서 서버에서 처리하고 처리 결과를 응답
- PUT : 서버에 데이터를 업데이트 하는 메소드, 요청한 데이터를 서버에 저장하고 처리를 응답
- DELETE : 서버에서 데이터를 삭제하는 메소드, 요청한 데이터를 서버에서 삭제하고 처리결과를 응답
</details>

---

<br />

### 캐시와 쿠키

<details>
  <summary>나의 답변 (👈 Click)</summary>

캐시는 웹 페이지나 리소스의 임시 저장소입니다.
웹 사이트의 로딩 속도를 개선하기 위해 사용됩니다.

메인페이지에 이미지를 변경했는데 실환경에 반영이 되고 있지 않는데요?
→ 혹시 캐시 지워보시겠어요?

---

쿠키는 사용자의 세션 정보나 설정을 저장하기 위해 클라이언트에 저장되는 작은 데이터 조각입니다.
인터넷 사용 기록이나 로그인 기록을 지우기 위해서는 쿠키를 제거하면 되는 경우가 이에 해당됩니다.

---

캐시는 브라우저 성능얼, 쿠키는 사용자 식별과 세션 관리를 돕습니다.

</details>

---

<br />

### 브라우저 렌더링 원리

<details>
  <summary>나의 답변 (👈 Click)</summary>

브라우저 렌더링은 HTML, CSS, JS를 화면에 그리는 과정입니다.

    1. DOM을 생성합니다.
    2. HTML 문서 파싱해서 돔트리를 생성합니다.
    → HTML 태그 노드로 변환
    3. CSS 파일 파싱해서 CSS트리를 생성합니다.
    → CSS 속성 노드로 변환
    4. HTML 돔트리와 CSS 트리를 결합합니다.
    5. 화면에 표시될 요소들을 선택해서 렌더트리를 생성합니다.
    6. 각 요소의 정확한 위치와 크기를 계산해서 화면에 그려줍니다.
        1. 레이아웃 위치를 계산하고 페인트 해준 후,

        2. 돔이나 CSS트리(CSSOM) 변경으로 레이아웃이 변경되면 리플로우가 발생합니다. (ex. `width`, `height`, `padding`, `margin` 등 변경)

        3. 요소나 전체를 다시 그리게 하면 리페인트가 발생합니다. (ex. `background-color`, `color`, `box-shadow` 등 변경)

        4. 리페인트는 레이아웃을 다시 계산할 필요가 없긴 하지만 픽셀을 다시 그려야 하기 때문에 성능에 영향을 줄 수 있고,
        리플로우는 레이아웃을 다시 계산해서 그려줘야하는 것이기 때문에 성능에 많은 영향을 줍니다.
        최대한 리플로우가 적도록 작업하는 것이 좋습니다.

</details>

---

<br />

### 스토리북(Storybook)에 대해서 아시나요?

<details>
  <summary>나의 답변 (👈 Click)</summary>

UI 컴포넌트 단위로 개발하기 위한 도구중 하나입니다.

공통 컴포넌트들을 모아서 문서화 하는 것에도 주로 사용됩니다.

각 컴포넌트별 기능과 상태를 여러 케이스별로 테스트 할 수 있습니다.

디자인 협업에서의 많은 도움이 됩니다.

</details>

---

<br />

### TDD란?(Test-Driven Development)

<details>
  <summary>나의 답변 (👈 Click)</summary>

**테스트 주도 개발 방법론**

개발자가 코드를 작성하기 전에 먼저 테스트 케이스를 작성하고 이를 통과시키는 것을 중심으로 개발을 진행하는 방법입니다.

TDD 도구 : Jest, testing-library 사용

</details>

---

<br />

### 비동기 함수에 대해서 설명해주세요.

<details>
  <summary>나의 답변 (👈 Click)</summary>

함수의 실행 결과가 다 완료 될때까지 기다리지 않고, 다음 작업으로 넘어가는 방식의 함수입니다.

비동기 함수는 작업이 완료될 때 **콜백함수, 프로미스, async/await** 을 통해 결과를 처리합니다.

---

**비동기 함수 사용시에 콜백지옥을 주의해야합니다**

비동기 작업이 여러단계로 연결될 때 단계별로 콜백함수가 필요해서 계단 마냥 들여쓰기가 깊어지는 문제를 콜백 지옥이라고 부릅니다.

해결 방법으로는,

1. `Promise`를 사용해서 `then()` 을 사용해서 성공시 처리되도록 합니다.

2. `async/await` 를 사용해서 `await` 키워드로 함수를 기다리게 했다가 실행시키도록 합니다.
</details>

---

<br />

### 라이브러리와 프레임워크의 차이점은?

<details>
  <summary>나의 답변 (👈 Click)</summary>

프레임워크는 전체적인 흐름을 자체적으로 가지고 있습니다.  
그 안에 필요한 코드를 작성합니다.

라이브러리는 개발자가 흐름에 대해 제어를 하고 필요한 상황에 가져다 쓸 수 있습니다.

---

**React는 자바스크립트 기반 라이브러리 이고,  
Next.js는 리액트를 기반응로 한 프레임워크 입니다.**

- **React**는 UI 인터페이스를 구축하기 위한 라이브러리로 컴포넌트 단위로 개발합니다.

- **Next**는 리액트 기능을 기반으로 애플리케이션의 기능과 구조를 설계할 수 있습니다.

- SSR, 파일기반 라우팅 등 개발자가 설계할 수 있습니다.

- 리액트를 더 확장해서 더 넓은 범위의 기능과 구조를 제공합니다.
</details>

---

<br />

### SSR과 CSR의 장단점에 대해서 설명해주세요.

<details>
  <summary>나의 답변 (👈 Click)</summary>

**SSR 장점**

- 서버에서 HTML을 미리 생성해서 전송하므로 초기 로드 시간이 빠릅니다. 사용자가 빨리 화면을 볼 수 있습니다.

- 검색 엔진이 쉽게 크롤링 할 수 있기 때문에 검색 엔진 최적화에 유리합니다.

**SSR 단점**

- 서버에서 부담해야할 요청이 많으면 서버에 부담이 될 수 있습니다.

- 초기 페이지 로드 후에, 클라이언트 쪽에서 추가적으로 자바스크립트를 로드 해야하기 때문에 인터렉션 기능이 있는 곳은 느려질 수 있습니다.

---

**CSR 장점**

- 클라이언트 측에서 대부분 렌더링 처리를 하기 때문에 서버 부담이 줍니다.

- 동적이고 복잡한 사용자 인터페이스를 쉽게! 구현할 수 있습니다.

**CSR 단점**

- 서비스에 사용되는 모~든 자바스크립트 파일을 클라이언트 쪽에 보내야 하기 때문에 초기 로드 속도가 느려질 수 있습니다.

- 자바스크립트 기반으로 로드되기 때문에 검색엔진 크롤링이 어렵습니다.

- 클라이언트 쪽의 브라우저 성능에 따라 성능 차이가 있을 수 있습니다. 의존적입니다.
</details>
