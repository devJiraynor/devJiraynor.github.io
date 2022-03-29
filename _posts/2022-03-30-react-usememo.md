---
layout: post
title: React 24. React useMemo 후크 (useMemo Hook)
subtitle: React useMemo Hook은 메모화된 값을 반환합니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React useMemo 후크

React ```useMemo``` Hook은 메모화된 값을 반환합니다.

{: .box-note}
메모화는 값을 캐시하는 것으로 간주하여 재계산할 필요가 없습니다.

```useMemo``` Hook은 의존관계 중 하나가 갱신되었을 때만 실행됩니다.

이를 통해 성능을 향상시킬 수 있습니다.

{: .box-note}
```useMemo```와 ```useCallback``` Hooks는 비슷합니다. 주요 차이점은 ```useMemo```는 메모화된 값을 반환하고 ```useCallback```은 메모화된 함수를 반환한다는 것입니다.

## 퍼포먼스

```useMemo``` Hook을 사용하면 비용이 많이 들고 리소스가 많이 사용되는 기능이 불필요하게 실행되지 않도록 할 수 있습니다.

이 예에서는 모든 렌더에서 실행되는 고비용의 함수를 사용하고 있습니다.

카운트를 변경하거나 작업을 추가할 때 실행이 지연됩니다.

###### 예제 - 성능이 저하되었습니다. ```hostCalculation``` 함수는 모든 렌더에서 실행됩니다.

```javascript
import { useState } from "react";
import ReactDOM from "react-dom";

const App = () => {
  const [count, setCount] = useState(0);
  const [todos, setTodos] = useState([]);
  const calculation = expensiveCalculation(count);

  const increment = () => {
    setCount((c) => c + 1);
  };
  const addTodo = () => {
    setTodos((t) => [...t, "New Todo"]);
  };

  return (
    <div>
      <div>
        <h2>My Todos</h2>
        {todos.map((todo, index) => {
          return <p key={index}>{todo}</p>;
        })}
        <button onClick={addTodo}>Add Todo</button>
      </div>
      <hr />
      <div>
        Count: {count}
        <button onClick={increment}>+</button>
        <h2>Expensive Calculation</h2>
        {calculation}
      </div>
    </div>
  );
};

const expensiveCalculation = (num) => {
  console.log("Calculating...");
  for (let i = 0; i < 1000000000; i++) {
    num += 1;
  }
  return num;
};

ReactDOM.render(<App />, document.getElementById('root'));
```

## ```useMemo``` 사용

이 성능 문제를 수정하려면 ```useMemo``` Hook을 사용하여 고비용의 계산 함수를 메모합니다. 그러면 필요할 때만 기능이 실행됩니다.

고비용의 함수 호출을 ```useMemo```로 랩할 수 있습니다.

```useMemo``` Hook은 의존관계를 선언하기 위한 두 번째 파라미터를 받아들입니다. 고비용 함수는 종속성이 변경되었을 때만 실행됩니다.

다음 예제에서는 고비용 함수는 ```count```가 변경되었을 때만 실행되며 작업관리가 추가되었을 때는 실행되지 않습니다.

###### 예제 - ```useMemo``` Hook을 사용한 퍼포먼스 향상

```javascript
import { useState, useMemo } from "react";
import ReactDOM from "react-dom";

const App = () => {
  const [count, setCount] = useState(0);
  const [todos, setTodos] = useState([]);
  const calculation = useMemo(() => expensiveCalculation(count), [count]);

  const increment = () => {
    setCount((c) => c + 1);
  };
  const addTodo = () => {
    setTodos((t) => [...t, "New Todo"]);
  };

  return (
    <div>
      <div>
        <h2>My Todos</h2>
        {todos.map((todo, index) => {
          return <p key={index}>{todo}</p>;
        })}
        <button onClick={addTodo}>Add Todo</button>
      </div>
      <hr />
      <div>
        Count: {count}
        <button onClick={increment}>+</button>
        <h2>Expensive Calculation</h2>
        {calculation}
      </div>
    </div>
  );
};

const expensiveCalculation = (num) => {
  console.log("Calculating...");
  for (let i = 0; i < 1000000000; i++) {
    num += 1;
  }
  return num;
};

ReactDOM.render(<App />, document.getElementById('root'));
```
