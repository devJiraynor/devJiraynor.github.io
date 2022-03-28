---
layout: post
title: React 19. React useEffect 후크 (useEffect Hook)
subtitle: useEffect Hook을 사용하면 컴포넌트에서 side effect를 수행할 수 있습니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React useEffect 후크

```useEffect``` Hook을 사용하면 컴포넌트에서 side effect를 수행할 수 있습니다.

side effect의 예로는 데이터 가져오기, DOM 직접 업데이트, 타이머 등이 있습니다.

```useEffect```에는 두 개의 인수를 사용할 수 있습니다. 두 번째 인수는 옵션입니다.

```useEffect(<function>, <dependency>)```

예시로 타이머를 사용해 봅시다.

##### 예제 1 - ```set Timeout()```을 사용하여 초기 렌더링 후 1초를 카운트합니다.

```javascript
import { useState, useEffect } from "react";
import ReactDOM from "react-dom";

function Timer() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    setTimeout(() => {
      setCount((count) => count + 1);
    }, 1000);
  });

  return <h1>I've rendered {count} times!</h1>;
}

ReactDOM.render(<Timer />, document.getElementById('root'));
```

그런데 잠깐!! 한 번만 세야 하는데 계속 세고 있습니다!

```useEffect```는 모든 렌더에서 실행됩니다. 즉, 카운트가 변경되면 렌더가 발생하며, 그 결과 다른 effect가 트리거됩니다.

이건 우리가 원하는게 아닙니다. side effect 시기를 조절하는 몇 가지 방법이 있다.

배열을 받아들이는 두 번째 매개 변수를 항상 포함해야 합니다. 옵션으로 종속성을 전달하여 이 배열에서 ```useEffect```를 사용할 수 있습니다.

###### 1. 종속성이 전달되지 않음

```javascript
useEffect(() => {
  // 모든 랜더에서 실행됨
});
```

###### 2. 빈 배열

```javascript
useEffect(() => {
  // 첫번째 랜더에서만 실행됨
}, []);
```

###### 3. props나 state 값

```javascript
useEffect(() => {
  // 첫번째 랜더에서 실행됨
  // props나 state가 변경될때 실행됨
}, [prop, state]);
```

이 문제를 해결하기위해 초기 렌더링에서만 이 effect를 실행해 보겠습니다.

###### 예제 2 - 초기 렌더링에만 effect를 실행합니다.

```javascript
import { useState, useEffect } from "react";
import ReactDOM from "react-dom";

function Timer() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    setTimeout(() => {
      setCount((count) => count + 1);
    }, 1000);
  }, []); // <- add empty brackets here

  return <h1>I've rendered {count} times!</h1>;
}

ReactDOM.render(<Timer />, document.getElementById('root'));
```

###### 예제 3 - 다음은 변수에 종속된 useEffect Hook의 예입니다. 카운트 변수가 업데이트되면 효과가 다시 실행됩니다.

```javascript
import { useState, useEffect } from "react";
import ReactDOM from "react-dom";

function Counter() {
  const [count, setCount] = useState(0);
  const [calculation, setCalculation] = useState(0);

  useEffect(() => {
    setCalculation(() => count * 2);
  }, [count]); // <- add the count variable here

  return (
    <>
      <p>Count: {count}</p>
      <button onClick={() => setCount((c) => c + 1)}>+</button>
      <p>Calculation: {calculation}</p>
    </>
  );
}

ReactDOM.render(<Counter />, document.getElementById('root'));
```

종속성이 여러 개인 경우 useEffect 종속성 배열에 포함해야 합니다.

## effect cleeanup

일부 effect는 메모리 누수를 줄이기 위해 cleanup이 필요합니다.

타임아웃, 서브스크립션, 이벤트 리스너 및 더 이상 필요하지 않은 기타 effect는 폐기해야 합니다.

이를 위해 ```useEffect``` Hook 끝에 반환 함수를 포함합니다.

###### 예제 4 - ```useEffect``` Hook 끝의 타이머를 cleanup 합니다.

```javascript
import { useState, useEffect } from "react";
import ReactDOM from "react-dom";

function Timer() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    let timer = setTimeout(() => {
    setCount((count) => count + 1);
  }, 1000);

  return () => clearTimeout(timer)
  }, []);

  return <h1>I've rendered {count} times!</h1>;
}

ReactDOM.render(<Timer />, document.getElementById("root"));
```

{: .box-note}
**Note:** 타이머를 클리어하기 위해서 이름을 붙여야 합니다.
