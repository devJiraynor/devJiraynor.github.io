---
layout: post
title: React 09. 이벤트 (Events)
subtitle: HTML DOM 이벤트와 마찬가지로 React는 사용자 이벤트를 기반으로 액션을 수행할 수 있습니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React 이벤트

HTML DOM 이벤트와 마찬가지로 React는 사용자 이벤트를 기반으로 액션을 수행할 수 있습니다.

리액트에는 HTML과 같은 이벤트(click, change, mouseover 등)가 있습니다.

## 이벤트 추가

React 이벤트는 카멜케이스 구문으로 작성됩니다.

```onclick``` 대신 ```onClick``` 을 사용합니다.

리액트 이벤트 핸들러는, 다음과 같이 중괄호로 둘러싸여 있습니다.

```onClick="shoot()"``` 대신 ```onClick={shoot}```을 사용합니다.

###### React

```javascript
<button onClick={shoot}>Take the Shot!</button>
```

###### HTML

```html
<button onclick="shoot()">Take the Shot!</button>
```

###### 예제 1 - ```shoot``` 함수를 ```Football``` 컴포넌트 안에 넣습니다.

```javascript
function Football() {
  const shoot = () => {
    alert("Great Shot!");
  }

  return (
    <button onClick={shoot}>Take the shot!</button>
  );
}

ReactDOM.render(<Football />, document.getElementById('root'));
```

## 인수 전달

이벤트 핸들러에 인수를 전달하려면 화살표 함수를 사용합니다.

###### 예제 2 - 화살표 함수fmf 사용하여 "Goal!"을 ```shoot``` 함수에 파라미터로 전송합니다.

```javascript
function Football() {
  const shoot = (a) => {
    alert(a);
  }

  return (
    <button onClick={() => shoot("Goal!")}>Take the shot!</button>
  );
}

ReactDOM.render(<Football />, document.getElementById('root'));
```

## React 이벤트 객체

이벤트 핸들러는 함수를 트리거한 React 이벤트에 액세스할 수 있습니다.

이 예에서 이벤트는 "click" 이벤트입니다.

###### 예제 3 - 화살표 함수: 이벤트 객체를 수동으로 보내는 방법

```javascript
function Football() {
  const shoot = (a, b) => {
    alert(b.type);
    /*
    'b' represents the React event that triggered the function,
    in this case the 'click' event
    */
  }

  return (
    <button onClick={(event) => shoot("Goal!", event)}>Take the shot!</button>
  );
}

ReactDOM.render(<Football />, document.getElementById('root'));
```
