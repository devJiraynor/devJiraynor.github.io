---
layout: post
title: React 18. React useState 후크 (useState Hook)
subtitle: React useState Hook을 사용하면 함수 컴포넌트의 상태를 추적할 수 있습니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React useState 후크

React ```useState``` Hook을 사용하면 함수 컴포넌트의 상태를 추적할 수 있습니다.

state는 일반적으로 응용 프로그램에서 추적해야 하는 데이터 또는 속성을 가리킵니다.

## ```useState``` import

```useState``` Hook을 사용하려면 먼저 컴포넌트로 ```import```해야 합니다.

###### 예제 1 - 컴포넌트 상단에서 ```useState``` Hook을 ```import```합니다.

```javascript
import { useState } from "react";
```

```useState```는 named export 이므로 ```react``` 에서 디스트럭팅됩니다.

## ```useState``` 초기화

함수 컴포넌트에서 ```useState```를 호출하여 ```state```를 초기화합니다.

```useState```는 초기 상태를 받아들이고 다음 두 가지 값을 반환합니다.

+ 현재 state
+ state를 갱신하는 함수.

###### 예제 2 - 함수 컴포넌트의 상단에서 state를 초기화합니다.

```javascript
import { useState } from "react";

function FavoriteColor() {
  const [color, setColor] = useState("");
}
```

여기서도 useState에서 반환된 값을 디스트럭팅하고 있습니다.

첫 번째 값인 ```color```는 현재 state입니다.

두 번째 값인 ```setColor```는 state를 갱신하기 위해 사용되는 함수입니다.

{: .box-note}
이러한 이름은 원하는 이름을 지정할 수 있는 변수입니다.

마지막으로 초기 state를 빈 문자열로 설정합니다. ```useState("")```

## state 읽기

이제 state를 컴포넌트 어디에서나 사용할 수 있습니다.

###### 예제 3 - 렌더링된 컴포넌트에서 state 변수를 사용합니다.

```javascript
import { useState } from "react";
import ReactDOM from "react-dom";

function FavoriteColor() {
  const [color, setColor] = useState("red");

  return <h1>My favorite color is {color}!</h1>
}

ReactDOM.render(<FavoriteColor />, document.getElementById('root'));
```

## state 수정

state를 수정하기 위해 stateSet 함수를 사용합니다.

{: .box-note}
state를 직접 수정해서는 안 됩니다. (예: color = "red"는 허용되지 않습니다.)

###### 예제 4 - 버튼을 사용하여 state를 수정합니다.

```javascript
import { useState } from "react";
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
    </>
  )
}

ReactDOM.render(<FavoriteColor />, document.getElementById('root'));
```

## state 홀딩 기능

```useState``` Hook을 사용하여 문자열, 숫자, 논리, 배열, 객체 및 이들의 조합을 추적할 수 있습니다.

개별 값을 추적하기 위해 여러 state Hook을 생성할 수 있습니다.

###### 예제 5 - 여러 state 후크 생성

```javascript
import { useState } from "react";
import ReactDOM from "react-dom";

function Car() {
  const [brand, setBrand] = useState("Ford");
  const [model, setModel] = useState("Mustang");
  const [year, setYear] = useState("1964");
  const [color, setColor] = useState("red");

  return (
    <>
      <h1>My {brand}</h1>
      <p>
        It is a {color} {model} from {year}.
      </p>
    </>
  )
}

ReactDOM.render(<Car />, document.getElementById('root'));
```

또는 하나의 state에 객체를 사용할 수도 있습니다.

###### 예제 6 - 객체를 가지는 단일 후크를 만듭니다.

```javascript
import { useState } from "react";
import ReactDOM from "react-dom";

function Car() {
  const [car, setCar] = useState({
    brand: "Ford",
    model: "Mustang",
    year: "1964",
    color: "red"
  });

  return (
    <>
      <h1>My {car.brand}</h1>
      <p>
        It is a {car.color} {car.model} from {car.year}.
      </p>
    </>
  )
}

ReactDOM.render(<Car />, document.getElementById('root'));
```

{: .box-note}
이제 단일 객체를 추적하고 있으므로 컴포넌트를 렌더링할 때 해당 객체를 참조하고 해당 객체의 속성을 참조해야 합니다(예: ```car.brand```).

## 객체 및 배열 state 수정

state가 갱신되면 state 전체가 덮어써집니다.

```car```의 ```color```만 업데이트하려면 어떻게 해야 할까요?

```setCar({color: "blue"})```만 호출하면 brand, model 및 year가 state에서 제거됩니다.

JavaScript spread 연산자를 사용하면 도움이 됩니다.

###### 예제 7 - JavaScript 확산 연산자를 사용하여 ```car```의 ```color``` 만 업데이트합니다.

```javascript
import { useState } from "react";
import ReactDOM from "react-dom";

function Car() {
  const [car, setCar] = useState({
    brand: "Ford",
    model: "Mustang",
    year: "1964",
    color: "red"
  });

  const updateColor = () => {
    setCar(previousState => {
      return { ...previousState, color: "blue" }
    });
  }

  return (
    <>
      <h1>My {car.brand}</h1>
      <p>
        It is a {car.color} {car.model} from {car.year}.
      </p>
      <button
        type="button"
        onClick={updateColor}
      >Blue</button>
    </>
  )
}

ReactDOM.render(<Car />, document.getElementById('root'));
```

현재 state 값이 필요하기 때문에 함수를 ```setCar``` 함수로 전달합니다. 이 함수는 이전 값을 수신합니다.

그런 다음 객체를 반환하고 ```previousState```를 확산 연산자로 받고 ```color```만 덮어씁니다.
