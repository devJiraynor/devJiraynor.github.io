---
layout: post
title: React 14. 메모 (Memo)
subtitle: memo를 사용하면 컴포넌트의 props가 변경되지 않은 경우 React는 구성요소의 렌더링을 건너뜁니다. 이를 통해 성능을 향상시킬 수 있습니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React memo

## 문제

이 예에서 ```Todos``` 컴포넌트는 ```todos```가 변경되지 않은 경우에도 다시 렌더링됩니다.

###### ```index.js```

```javascript
import { useState } from "react";
import ReactDOM from "react-dom";
import Todos from "./Todos";

const App = () => {
  const [count, setCount] = useState(0);
  const [todos, setTodos] = useState(["todo 1", "todo 2"]);

  const increment = () => {
    setCount((c) => c + 1);
  };

  return (
    <>
      <Todos todos={todos} />
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

###### ```Todo.js```

```javascript
const Todos = ({ todos }) => {
  console.log("child render");
  return (
    <>
      <h2>My Todos</h2>
      {todos.map((todo, index) => {
        return <p key={index}>{todo}</p>;
      })}
    </>
  );
};

export default Todos;
```

버튼을 클릭하면 ```Todos``` 컴포넌트가 다시 렌더링됩니다.

이 경우 컴포넌트가 복잡하면 퍼포먼스 문제가 발생할 수 있습니다.

## 해결책

이 문제를 해결하기 위해 memo를 사용할 수 있습니다.

```memo```를 사용하여 ```Todos``` 컴포넌트의 불필요한 재렌더링을 방지합니다.

```Todos``` 구성 요소 내보내기를 ```memo```로 래핑합니다.

###### ```index.js```

```javascript
import { useState } from "react";
import ReactDOM from "react-dom";
import Todos from "./Todos";

const App = () => {
  const [count, setCount] = useState(0);
  const [todos, setTodos] = useState(["todo 1", "todo 2"]);

  const increment = () => {
    setCount((c) => c + 1);
  };

  return (
    <>
      <Todos todos={todos} />
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

###### ```Todo.js```

```javascript
import { memo } from "react";

const Todos = ({ todos }) => {
  console.log("child render");
  return (
    <>
      <h2>My Todos</h2>
      {todos.map((todo, index) => {
        return <p key={index}>{todo}</p>;
      })}
    </>
  );
};

export default memo(Todos);
```

이제 ```Todos``` 컴포넌트는 props를 통해 전달되는 ```todos```가 업데이트될 때만 다시 렌더링됩니다.
