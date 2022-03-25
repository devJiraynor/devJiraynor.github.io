---
layout: post
title: React 10. 조건부 렌더링 (Conditional Rendering)
subtitle: React에서 컴포넌트를 조건부로 렌더링할 수 있습니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React 조건부 렌더링

## ```if``` 구문

```if``` JavaScript 연산자를 사용하여 렌더링할 컴포넌트를 결정할 수 있습니다.

###### 예제 1 - 다음 두 가지 컴포넌트를 사용합니다.

```javascript
function MissedGoal() {
  return <h1>MISSED!</h1>;
}

function MadeGoal() {
  return <h1>Goal!</h1>;
}
```

###### 예제 2 - 이제 조건에 따라 렌더링할 컴포넌트를 선택하는 다른 컴포넌트를 만듭니다.

```javascript
function Goal(props) {
  const isGoal = props.isGoal;
  if (isGoal) {
    return <MadeGoal/>;
  }
  return <MissedGoal/>;
}

ReactDOM.render(
  <Goal isGoal={false} />,
  document.getElementById('root')
);
```

```isGoal``` 속성을 ```true```로 변경해 보겠습니다.

###### 예제 3

```javascript
ReactDOM.render(
  <Goal isGoal={true} />,
  document.getElementById('root')
);
```

## ```&&``` 논리 연산자

React 컴포넌트를 조건부로 렌더링하는 또 다른 방법은 ```&&``` 연산자를 사용하는 것입니다.

###### 예제 4 - JavaScript 표현식을 JSX에 포함하려면 중괄호를 사용합니다.

```javascript
function Garage(props) {
  const cars = props.cars;
  return (
    <>
      <h1>Garage</h1>
      {cars.length > 0 &&
        <h2>
          You have {cars.length} cars in your garage.
        </h2>
      }
    </>
  );
}

const cars = ['Ford', 'BMW', 'Audi'];
ReactDOM.render(
  <Garage cars={cars} />,
  document.getElementById('root')
);
```

```cars.length```가 ```true``` 인 경우 ```&&``` 뒤의 식이 렌더링됩니다.

```cars``` 배열을 비워보세요.

###### 예제 5

```javascript
const cars = [];
ReactDOM.render(
  <Garage cars={cars} />,
  document.getElementById('root')
);
```

## 삼항 연산자

요소를 조건부로 렌더링하는 또 다른 방법은 삼항 연산자를 사용하는 것입니다.

```javascript
condition ? true : false
```

###### 예제 6 - ```isGoal```이 ```true``` 이면 ```MadeGoal``` 컴포넌트를 반환하고 그렇지 않으면 ```MissedGoal``` 컴포넌트를 반환합니다.

```javascript
function Goal(props) {
  const isGoal = props.isGoal;
  return (
    <>
      { isGoal ? <MadeGoal/> : <MissedGoal/> }
    </>
  );
}

ReactDOM.render(
  <Goal isGoal={false} />,
  document.getElementById('root')
);
```
