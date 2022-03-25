---
layout: post
title: React 08. Props
subtitle: props는 React 컴포넌트에 전달되는 인수입니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React Props

props는 React 컴포넌트에 전달되는 인수입니다.

props는 HTML 속성을 통해 컴포넌트에 전달됩니다.

{: .box-note}
```props```는 프로퍼티를 나타냅니다.

## React Props

React에서 ```proprs``` 는 JavaScript의 함수의 파라미터와 HTML의 속성과 같습니다.

컴포넌트에 ```props```를 보내려면 HTML 속성과 동일한 구문을 사용합니다.

###### 예제 1 - Car 요소에 "brand" 속성을 추가

```javascript
const myelement = <Car brand="Ford" />;
```

컴포넌트는 파라미터를 ```props``` 객체로 수신합니다.

###### 예제 2 - 컴포넌트에서 "brand" 속성 사용

```javascript
function Car(props) {
  return <h2>I am a { props.brand }!</h2>;
}
```

## 데이터 전달

```props```는 한 컴포넌트에서 다른 컴포넌트로 데이터를 전달하는 방법입니다.

###### 예제 3 - Garage 컴포넌트에서 Car 컴포넌트로 "brand" 속성 전송

```javascript
function Car(props) {
  return <h2>I am a { props.brand }!</h2>;
}

function Garage() {
  return (
    <>
      <h1>Who lives in my garage?</h1>
      <Car brand="Ford" />
    </>
  );
}

ReactDOM.render(<Garage />, document.getElementById('root'));
```

위의 예시와 같이 문자열이 아닌 전송할 변수가 있는 경우 변수 이름을 중괄호 안에 넣습니다.

###### 예제 4 - carName이라는 이름의 변수를 생성하여 Car 컴포넌트로 전송

```javascript
function Car(props) {
  return <h2>I am a { props.brand }!</h2>;
}

function Garage() {
  const carName = "Ford";
  return (
    <>
      <h1>Who lives in my garage?</h1>
      <Car brand={ carName } />
    </>
  );
}

ReactDOM.render(<Garage />, document.getElementById('root'));
```

만약 객체일 경우 아래와 같이 사용합니다.

###### 예제 5 - carInfo라는 객체를 생성하여 Car 컴포넌트로 전송

```javascript
function Car(props) {
  return <h2>I am a { props.brand.model }!</h2>;
}

function Garage() {
  const carInfo = { name: "Ford", model: "Mustang" };
  return (
    <>
      <h1>Who lives in my garage?</h1>
      <Car brand={ carInfo } />
    </>
  );
}

ReactDOM.render(<Garage />, document.getElementById('root'));
```

{: .box-note}
React Props는 읽기 전용입니다! 값을 변경하려고 하면 오류가 발생합니다.
