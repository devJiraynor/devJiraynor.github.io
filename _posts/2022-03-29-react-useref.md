---
layout: post
title: React 21. React useRef 후크 (useRef Hook)
subtitle: useRef Hook을 사용하면 렌더링 간에 값을 유지할 수 있습니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React ```useRef``` 후크

useRef Hook을 사용하면 렌더링 간에 값을 유지할 수 있습니다.

업데이트 시 재렌더가 발생하지 않는 가변 값을 저장하는 데 사용할 수 있습니다.

DOM 요소에 직접 액세스하기 위해 사용할 수 있습니다.

## 재렌더 발생 안 함

어플리케이션이 ```useState``` Hook을 사용하여 렌더링하는 횟수를 세면 이 Hook 자체가 리렌더를 일으키기 때문에 무한 루프에 빠집니다.

이를 피하기 위해 ```useRef``` Hook을 사용할 수 있습니다.

###### 예제 - ```useRef```를 사용하여 응용 프로그램 렌더링을 추적합니다.

```javascript
import { useState, useEffect, useRef } from "react";
import ReactDOM from "react-dom";

function App() {
  const [inputValue, setInputValue] = useState("");
  const count = useRef(0);

  useEffect(() => {
    count.current = count.current + 1;
  });

  return (
    <>
      <input
        type="text"
        value={inputValue}
        onChange={(e) => setInputValue(e.target.value)}
      />
      <h1>Render Count: {count.current}</h1>
    </>
  );
}

ReactDOM.render(<App />, document.getElementById('root'));
```

```useRef()```는 하나의 항목만 반환합니다. ```current```라는 객체를 반환합니다.

```useRef```를 초기화할 때 초기값 ```useRef(0)```를 설정합니다.

{: .box-note}
```useRef(0)```은 ```const count = { current : 0 }```와 같습니다. ```count.current```를 사용하여 카운트에 액세스할 수 있습니다.

## DOM 요소 접근

일반적으로는 React가 모든 DOM 조작을 처리하도록 합니다.

그러나 문제를 일으키지 않고 ```useRef```를 사용할 수 있는 경우가 있습니다.

React에서는 요소에 ```ref``` 속성을 추가하여 DOM에서 직접 액세스할 수 있습니다.

###### 예제 - ```useRef```를 사용하여 input에 포커스를 맞춥니다.

```javascript
import { useRef } from "react";
import ReactDOM from "react-dom";

function App() {
  const inputElement = useRef();

  const focusInput = () => {
    inputElement.current.focus();
  };

  return (
    <>
      <input type="text" ref={inputElement} />
      <button onClick={focusInput}>Focus Input</button>
    </>
  );
}

ReactDOM.render(<App />, document.getElementById('root'));
```

## state 변경 추적

```useRef``` Hook을 사용하여 이전 state 값을 추적할 수도 있습니다.

이는 렌더링 간에 ```useRef``` 값을 유지할 수 있기 때문입니다.

###### 예제 - 이전 state 값을 추적하려면 ```useRef```를 사용합니다.

```javascrip
import { useState, useEffect, useRef } from "react";
import ReactDOM from "react-dom";

function App() {
  const [inputValue, setInputValue] = useState("");
  const previousInputValue = useRef("");

  useEffect(() => {
    previousInputValue.current = inputValue;
  }, [inputValue]);

  return (
    <>
      <input
        type="text"
        value={inputValue}
        onChange={(e) => setInputValue(e.target.value)}
      />
      <h2>Current Value: {inputValue}</h2>
      <h2>Previous Value: {previousInputValue.current}</h2>
    </>
  );
}

ReactDOM.render(<App />, document.getElementById('root'));
```

이번에는 ```useState```, ```useEffect``` 및 ```useRef```의 조합을 사용하여 이전 state를 추적합니다.

```useEffect```에서는 input 필드에 텍스트를 입력하여 ```inputValue```가 갱신될 때마다 ```useRef``` 현재 값을 갱신하고 있습니다.
