# JavaScript

<br />

### async/await 에 대해서 설명해주세요.

<details>
  <summary>나의 답변 (👈 Click)</summary>

<br />

`async`와 `await`는 자바스크립트에서 비동기 작업을 처리하기 위한 문법입니다.

- `async` 키워드를 사용한 함수는 자동으로 Promise 객체를 반환하는 비동기 함수가 됩니다.

- `await` 키워드는 비동기 작업이 완료될 때까지 함수를 일시 중지하고, 완료된 후 결과값을 반환합니다.

  `await`는 반드시 `async` 함수 내에서만 사용 가능합니다.

  API 호출하기 위해 `fetch` 를 사용할 때 데이터를 비동기적으로 가져오고,
  가져온 데이터를 JSON으로 변환하는 작업 모두 비동기 함수입니다.

  그래서 이것을 처리할 때 두 단계에서 `await` 를 사용해서 비동기 작업을 순서대로 처리할 수 있습니다.

  ```tsx
  async function fetchData() {
    const response = await fetch('https://www.example.api/');
    const data = await response.json();
    return data;
  }
  ```

<br />

**동기**

- 요청과 결과가 순차적으로 처리됩니다.
- 먼저 실행된 작업이 끝나야 다음 작업을 실행할 수 있습니다.
- 여러 요청을 동시에 처리하지 못합니다.

<br />

**비동기**

- 요청과 결과가 동시에 처리되지 않을 수 있습니다.
- 비동기 함수는 실행된 작업이 대기 시간과 상관없이 다른 작업을 동시에 처리할 수 있습니다.
- 여러 요청을 동시에 처리할 수 있습니다.
</details>

---

<br />

### 여러 ajax 요청을 병렬로 처리하는 방법은?

<details>
  <summary>나의 답변 (👈 Click)</summary>

<br />

`Promise.all()`을 사용해서 모든 요청이 완료될 때 까지 기다리는 것입니다.

`Promise.all()`은 **주어진 모든 프로미스가 이행될때까지 기다린 후**, 결과를 **배열로 반환**합니다.

</details>

---

<br />

### 불변성에 대해서 설명해주세요.

<details>
  <summary>나의 답변 (👈 Click)</summary>

<br />

불변성은 데이터를 변경할 때 기존 데이터를 직접 수정하지 않고,
기존 데이터를 복사한 후 새로운 값을 반영하여 수정하는 프로그래밍 원칙입니다.

배열을 조작해야할 때 `map`, `filter`, `slice` 등을 사용해서 새로운 배열을 반환할 수 있도록 할 수 있습니다.

</details>

<br />

---

<br />

### 호이스팅에 대해서 설명해주세요.

<details>
  <summary>나의 답변 (👈 Click)</summary>

<br />

변수 혹은 함수 선언이 스코프(코드)의 최상단으로 올려져 실행되는 것을 말합니다.

자바스크립트 엔진이 먼저 전체 코드를 쭉 스캔하고 미리 기록해놓기 때문에 호이스팅 현상이 발생하는데, 실제로 코드가 옮겨지는 것은 아닙니다.

<br />

- `var` 로 변수를 선언하는 경우!

  ```jsx
  console.log(name); // undefined
  var name = 'gildong';
  console.log(name); // "gildong"
  ```

  - 변수 선언하기 전에 호출되는 경우 초기화 된 `var name;` 을 호출하게됩니다.

  - undefined로 나오고, 에러가 나지는 않습니다.

- `var` 에 대한 단점을 보완하기 위해서 나온 것이 `const`, `let` 은 먼저 선언하면 에러가 납니다.

  - 하지만 호이스팅이 안되는 것은 아닙니다.

  ```jsx
  console.log(name); // ReferenceError: Cannot access 'name' before initialization
  const name = 'gildong';
  console.log(name); // "gildong"
  ```

  - 호이스팅은 여전히 되고 있지만, undefined로 나오는것이 아닌 ReferenceError 에러가 발생하여 접근하지 못하게 되도록 합니다.

  - 선언 전에 작성된 `console.log(name)`의 zone은 일시적으로 죽은 구역이라고 불려 **TDZ(Temporal Dead Zone)** 이라고 합니다.

</details>

<br />

---

<br />

### 이벤트 버블링에 대해서 설명해주세요. 추가로 캡처링과 차이점은 무엇일까요?

<details>
  <summary>나의 답변 (👈 Click)</summary>

<br />

돔에서 이벤트가 발생했을 때 해당 요소에서 이벤트 처리가 된 후, **상위 요소로 이벤트가 전파되는 현상**을 말합니다.

버블링과 캡처링 둘다 이벤트가 전파되는 두가지 방식입니다.

**버블링은** 처리해야 하는 이벤트 함수를 부모 요소에 등록해 놓으면 자식 요소에서도 해당 이벤트를 모두 처리할 수 있는 것입니다.

⇒ 가장 안쪽 요소에서 시작해서 부모 요소를 거쳐 최상위 루트까지 전파됩니다.

**캡처링은** 버블링과 반대로 이벤트가 최상위 루트에서 시작해서 자식요소를 향해 전파됩니다.

버블링과 캡쳐링을 방지하기 위해서는 `stopPropagation()` 메서드를 사용해서 이벤트 전파를 중지시켜야합니다.

- **버블링 :** `child`요소를 클릭하면 `child`의 이벤트가 먼저 발생한 후, `parent`로 이벤트가 전파됩니다.
- **캡처링 :** `child`를 클릭하면 이벤트가 먼저 `parent`에서 발생한 후, `child`로 전파됩니다.

</details>

<br />
