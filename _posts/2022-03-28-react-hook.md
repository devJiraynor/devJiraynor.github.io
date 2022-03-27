---
layout: post
title: React 17. React 후크 (Hooks)
subtitle: 후크를 사용하면 함수 컴포넌트가 state 및 기타 React 기능에 액세스할 수 있습니다. 이 때문에 클래스 컴포넌트는 일반적으로 더 이상 필요하지 않습니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React Hooks

버전 16.8에서 후크가 React에 추가되었습니다.

후크를 사용하면 함수 컴포넌트가 state 및 기타 React 기능에 액세스할 수 있습니다. 이 때문에 클래스 컴포넌트는 일반적으로 더 이상 필요하지 않습니다.

{: .box-note}
일반적으로 Hooks는 클래스 컴포넌트를 대체하지만 React에서 클래스를 삭제할 계획은 없습니다.

## 후크란?

후크를 사용하면 state 및 생명주기 함수 등의 React 기능에 "후크"할 수 있습니다.

후크의 예를 다음에 나타냅니다. 이해가 안 된다고 걱정하지 마세요. 자세한 내용은 다음 섹션에서 설명하겠습니다.

###### 예제 - 1

```javascript
import React, { useState } from "react";
import ReactDOM from "react-dom";

function FavoriteColor() {
  const [color, setColor] = useState("red");

  return (
    <>
      <h1>My favorite color is {color}!</h1>
      <button
        type="button"
        onClick={() => setColor("blue")}
      >Blue</button>
      <button
        type="button"
        onClick={() => setColor("red")}
      >Red</button>
      <button
        type="button"
        onClick={() => setColor("pink")}
      >Pink</button>
      <button
        type="button"
        onClick={() => setColor("green")}
      >Green</button>
    </>
  );
}

ReactDOM.render(<FavoriteColor />, document.getElementById('root'));
```

```react```에서 Hooks를 ```import```해야 합니다.

여기에서는 ```useState``` Hook을 사용하여 응용 프로그램 상태를 추적합니다.

state는 일반적으로 추적해야 하는 응용 프로그램 데이터 또는 속성을 가리킵니다.

## 후크 규칙

후크에는 3가지 규칙이 있습니다.

+ 후크는 React 함수 컴포넌트 내에서만 호출할 수 있습니다.
+ 후크는 컴포넌트의 최상위 레벨에서만 호출할 수 있습니다.
+ 후크는 조건부일 수 없습니다.

{: .box-note}
후크는 React 클래스의 컴포넌트에서는 동작하지 않습니다.
