---
layout: post
title: React 23. React useCallback 후크 (useCallback Hook)
subtitle: React useCallback Hook은 메모화된 콜백 함수를 반환합니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React useCallback 후크

React useCallback Hook은 메모화된 콜백 함수를 반환합니다.

{: .box-note}
메모화(memorization)는 값을 캐시하는 것으로 간주하여 재계산할 필요가 없습니다.

이를 통해 리소스를 많이 사용하는 함수를 분리하여 모든 렌더링에서 자동으로 실행되지 않도록 할 수 있습니다.

```useCallback``` Hook은 의존관계 중 하나가 갱신되었을 때만 실행됩니다.

이를 통해 성능을 향상시킬 수 있습니다.

{: .box-note}
```useCallback```과 ```useMemo``` Hooks는 비슷합니다. 주요 차이점은 ```useMemo```는 메모화된 값을 반환하고 ```useCallback```은 메모화된 함수를 반환한다는 것입니다.

## 문제

```useCallback```을 사용하는 이유 중 하나는 컴포넌트의 props가 변경되지 않는 한 컴포넌트의 재렌더링을 방지하기 위함입니다.

이 예에서는 ```Todos``` 컴포넌트를 변경하지 않으면 ```Todos``` 컴포넌트가 다시 렌더링되지 않는다고 생각할 수 있습니다.

###### index.js

```javascript
import { useState } from "react";
import ReactDOM from "react-dom";
import Todos from "./Todos";

const App = () => {
  const [count, setCount] = useState(0);
  const [todos, setTodos] = useState([]);

  const increment = () => {
    setCount((c) => c + 1);
  };
  const addTodo = () => {
    setTodos((t) => [...t, "New Todo"]);
  };

  return (
    <>
      <Todos todos={todos} addTodo={addTodo} />
      <hr />
      <div>
        Count: {count}
        <button onClick={increment}>+</button>
      </div>
    </>
  );
};

ReactDOM.render(<App />, document.getElementById('root'));
```

###### Todos.js

```javascript
import { memo } from "react";

const Todos = ({ todos, addTodo }) => {
  console.log("child render");
  return (
    <>
      <h2>My Todos</h2>
      {todos.map((todo, index) => {
        return <p key={index}>{todo}</p>;
      })}
      <button onClick={addTodo}>Add Todo</button>
    </>
  );
};

export default memo(Todos);
```

실행후 count increment 버튼을 클릭합니다.

```Todos``` 컴포넌트는 ```Todos```가 변경되지 않은 경우에도 다시 렌더링됩니다.

```memo```는 사용 중이기 때문에 카운트가 증가해도 ```Todos``` state나 ```addTodo``` 함수는 변경되지 않으므로 ```Todos``` 컴포넌트는 다시 렌더링되지 않습니다.

이것은 "referential equality"이라고 불리는 것 때문이다.

컴포넌트가 재렌더될 때마다 그 기능이 재현됩니다. 이 때문에 ```addToDo``` 함수는 실제로 변경되었습니다.

## 해결책

이 문제를 해결하려면 ```useCallback``` Hook을 사용하여 필요한 경우를 제외하고 함수가 재생성되지 않도록 할 수 있습니다.

```useCallback``` Hook을 사용하여 ```Todos``` 컴포넌트가 불필요하게 재렌더되지 않도록 합니다.

###### index.js

```javascript
import { useState, useCallback } from "react";
import ReactDOM from "react-dom";
import Todos from "./Todos";

const App = () => {
  const [count, setCount] = useState(0);
  const [todos, setTodos] = useState([]);

  const increment = () => {
    setCount((c) => c + 1);
  };
  const addTodo = useCallback(() => {
    setTodos((t) => [...t, "New Todo"]);
  }, [todos]);

  return (
    <>
      <Todos todos={todos} addTodo={addTodo} />
      <hr />
      <div>
        Count: {count}
        <button onClick={increment}>+</button>
      </div>
    </>
  );
};

ReactDOM.render(<App />, document.getElementById('root'));
```

###### Todos.js

```javascript
import { memo } from "react";

const Todos = ({ todos, addTodo }) => {
  console.log("child render");
  return (
    <>
      <h2>My Todos</h2>
      {todos.map((todo, index) => {
        return <p key={index}>{todo}</p>;
      })}
      <button onClick={addTodo}>Add Todo</button>
    </>
  );
};

export default memo(Todos);
```

이제 ```Todos``` 컴포넌트는 ```Todos prop```가 변경될 때만 다시 렌더링됩니다.
