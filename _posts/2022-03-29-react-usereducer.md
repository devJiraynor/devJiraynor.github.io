---
layout: post
title: React 22. React useReducer 후크 (useReducer Hook)
subtitle: 복잡한 논리에 의존하는 여러 상태를 추적하는 경우 useReducer가 유용할 수 있습니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React ```useReducer``` 후크

```useReducer``` Hook은 ```useState``` Hook과 비슷합니다.

custom state 로직이 가능합니다.

복잡한 논리에 의존하는 여러 상태를 추적하는 경우 ```useReducer```가 유용할 수 있습니다.

## 구문

```useReducer``` Hook은 2개의 인수를 받아들입니다.

{: .box-note}
```useReducer(<reducer>, <initialState>)```
  
```reducer``` 함수에는 custom state 로직이 포함되어 있으며 ```initialState```는 단순한 값이지만 일반적으로 오브젝트가 포함됩니다.

```useReducer``` Hook은 현재 ```state```와 ```dispatch``` 방식을 반환합니다.

카운터 앱의 ```useReducer```의 예를 다음에 나타냅니다.

###### 예제

```javascript
import { useReducer } from "react";
import ReactDOM from "react-dom";

const initialTodos = [
  {
    id: 1,
    title: "Todo 1",
    complete: false,
  },
  {
    id: 2,
    title: "Todo 2",
    complete: false,
  },
];

const reducer = (state, action) => {
  switch (action.type) {
    case "COMPLETE":
      return state.map((todo) => {
        if (todo.id === action.id) {
          return { ...todo, complete: !todo.complete };
        } else {
          return todo;
        }
      });
    default:
      return state;
  }
};

function Todos() {
  const [todos, dispatch] = useReducer(reducer, initialTodos);

  const handleComplete = (todo) => {
    dispatch({ type: "COMPLETE", id: todo.id });
  };

  return (
    <>
      {todos.map((todo) => (
        <div key={todo.id}>
          <label>
            <input
              type="checkbox"
              checked={todo.complete}
              onChange={() => handleComplete(todo)}
            />
            {todo.title}
          </label>
        </div>
      ))}
    </>
  );
}

ReactDOM.render(<Todos />, document.getElementById('root'));
```

이것은 ```todo```의 완료 state를 추적하기 위한 논리입니다.

작업을 추가, 삭제 및 완료하기 위한 모든 논리를 단일 ```useReducer``` Hook 내에 포함할 수 있습니다.
