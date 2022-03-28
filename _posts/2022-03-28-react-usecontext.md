---
layout: post
title: React 20. React useContext 후크 (useContext Hook)
subtitle: React Context는 state를 전역으로 관리하는 방법입니다. useState Hook과 함께 사용하면 useState만 사용하는 것보다 더 쉽게 중첩된 구성 요소 간에 상태를 공유할 수 있습니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React useContext 후크

## React Context

React Context는 state를 전역으로 관리하는 방법입니다. 
```useState``` Hook과 함께 사용하면 ```useState```만 사용하는 것보다 더 쉽게 중첩된 구성 요소 간에 상태를 공유할 수 있습니다.

## 문제

state는 state에 대한 액세스가 필요한 스택의 상위 컴포넌트에 의해 유지되어야 합니다.

예를 들어, 여러 개의 중첩된 컴포넌트가 있습니다. 스택의 상단과 하단의 컴포넌트는 state에 액세스 할 필요가 있습니다.

context를 사용하지 않고 이를 수행하려면 중첩된 각 컴포넌트를 통해 state를 "prop"로 전달해야 합니다. 이것은 "props drilling"이라고 불립니다.

###### 예제 1 - 중첩된 컴포넌트를 통해 "props" 전달

```javascript
import { useState } from "react";
import ReactDOM from "react-dom";

function Component1() {
  const [user, setUser] = useState("Jesse Hall");

  return (
    <>
      <h1>{`Hello ${user}!`}</h1>
      <Component2 user={user} />
    </>
  );
}

function Component2({ user }) {
  return (
    <>
      <h1>Component 2</h1>
      <Component3 user={user} />
    </>
  );
}

function Component3({ user }) {
  return (
    <>
      <h1>Component 3</h1>
      <Component4 user={user} />
    </>
  );
}

function Component4({ user }) {
  return (
    <>
      <h1>Component 4</h1>
      <Component5 user={user} />
    </>
  );
}

function Component5({ user }) {
  return (
    <>
      <h1>Component 5</h1>
      <h2>{`Hello ${user} again!`}</h2>
    </>
  );
}

ReactDOM.render(<Component1 />, document.getElementById("root"));
```

컴포넌트 2-4는 state를 필요로 하지 않지만 컴포넌트 5에 도달할 수 있도록 state를 전달해야 했습니다.

## 해결책

해결책은 context를 작성하는 것입니다.

#### context 생성

context를 생성하려면 ```createContext```를 import하여 초기화해야 합니다.

```javascript
import { useState, createContext } from "react";
import ReactDOM from "react-dom";

const UserContext = createContext()
```

다음으로 context 공급자를 사용하여 state context가 필요한 컴포넌트 트리를 랩합니다.

```javascript
function Component1() {
  const [user, setUser] = useState("Jesse Hall");

  return (
    <UserContext.Provider value={user}>
      <h1>{`Hello ${user}!`}</h1>
      <Component2 user={user} />
    </UserContext.Provider>
  );
}
```

이제 이 트리의 모든 컴포넌트가 user context에 액세스할 수 있습니다.

#### ```useContext``` 후크 사용

자식 컴포넌트에서 context를 사용하려면 ```useContext``` Hook을 사용하여 액세스해야 합니다.

첫 번째로 ```useContext```를 import합니다.

```javascript
import { useState, createContext, useContext } from "react";
```

이제 모든 컴포넌트에서 user context에 액세스할 수 있습니다.

```javascript
function Component5() {
  const user = useContext(UserContext);

  return (
    <>
      <h1>Component 5</h1>
      <h2>{`Hello ${user} again!`}</h2>
    </>
  );
}
```

## 전체 예제

```javascript
import { useState, createContext, useContext } from "react";
import ReactDOM from "react-dom";

const UserContext = createContext();

function Component1() {
  const [user, setUser] = useState("Jesse Hall");

  return (
    <UserContext.Provider value={user}>
      <h1>{`Hello ${user}!`}</h1>
      <Component2 user={user} />
    </UserContext.Provider>
  );
}

function Component2() {
  return (
    <>
      <h1>Component 2</h1>
      <Component3 />
    </>
  );
}

function Component3() {
  return (
    <>
      <h1>Component 3</h1>
      <Component4 />
    </>
  );
}

function Component4() {
  return (
    <>
      <h1>Component 4</h1>
      <Component5 />
    </>
  );
}

function Component5() {
  const user = useContext(UserContext);

  return (
    <>
      <h1>Component 5</h1>
      <h2>{`Hello ${user} again!`}</h2>
    </>
  );
}

ReactDOM.render(<Component1 />, document.getElementById("root"));
```
