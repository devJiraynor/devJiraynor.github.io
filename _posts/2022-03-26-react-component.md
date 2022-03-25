---
layout: post
title: React 06. 컴포넌트 (Components)
subtitle: 컴포넌트는 HTML 요소를 반환하는 함수와 같습니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React 컴포넌트

## React 컴포넌트

컴포넌트는 독립된 재사용 가능한 코드 비트입니다. 이들은 JavaScript 함수와 동일한 목적을 수행하지만 독립적으로 작동하며 HTML을 반환합니다.

컴포넌트는 Class 컴포넌트와 Function 컴포넌트의 두 가지 타입이 있으며, 여기서는 Function 컴포넌트에 초점을 맞춥니다.

{: .box-note}
이전 React 코드 베이스에서는 주로 사용되는 Class 컴포넌트를 찾을 수 있습니다. 이제 React 16.8에서 추가된 Hooks와 함께 Function 컴포넌트를 사용하는 것이 좋습니다. 참조용으로 클래스 컴포넌트에 대한 옵션 섹션이 있습니다.

## 첫 번째 컴포넌트 작성

React 구성 요소를 생성할 때 구성 요소 이름은 **반드시** 대문자로 시작해야 합니다.

#### Class 컴포넌트

클래스 컴포넌트에는 ```extends React.Component``` 문이 포함되어야 합니다. 이 문은 ```React.Component```에 대한 상속을 생성하고 구성 요소가 ```React.Component```의 함수에 액세스할 수 있도록 합니다.

컴포넌트에는 ```render()``` 메서드도 필요합니다.이 메서드는 HTML을 반환합니다.

###### 예제 1 - Car class 컴포넌트 만들기

```javascript
class Car extends React.Component {
  render() {
    return <h2>Hi, I am a Car!</h2>;
  }
}
```

#### Fuction 컴포넌트

위의 예와 동일하지만 Function 컴포넌트를 사용하여 작성된 예를 다음에 나타냅니다.

함수 컴포넌트도 HTML을 반환하고 클래스 컴포넌트와 거의 동일하게 동작하지만 함수 컴포넌트는 훨씬 적은 코드로 기술할 수 있고 이해하기 쉽습니다.

###### 예제 2 - Car function 컴포넌트 만들기

```javascript
function Car() {
  return <h2>Hi, I am a Car!</h2>;
}
```

## 컴포넌트 랜더링

이제 React 어플리케이션에는 ```<h2>``` 요소를 반환하는 Car라는 컴포넌트가 있습니다.

응용 프로그램에서 이 컴포넌트를 사용하려면 일반 HTML과 동일한 구문을 사용합니다. ```< Car / >```

###### 예제 3 - "root" 요소에 Car 컴포넌트 출력하기

```javascript
ReactDOM.render(<Car />, document.getElementById('root'));
```

## Props

컴포넌트는 속성을 나타내는 ```props```로 전달할 수 있습니다.

```props```는 함수 파라미터와 같으며, 속성으로 컴포넌트에 보냅니다.

###### 예제 4 - 속성을 사용하여 색상을 Car 컴포넌트에 전달하고 render() 함수로 사용

```javascript
function Car(props) {
  return <h2>I am a {props.color} Car!</h2>;
}

ReactDOM.render(<Car color="red"/>, document.getElementById('root'));
```

## 컴포넌트 안의 컴포넌트

다른 컴포넌트 내부의 컴포넌트를 참조할 수 있습니다.

###### 예제 5 - Garage 컴포넌트 내에서 Car 컴포넌트를 사용

```javascript
function Car() {
  return <h2>I am a Car!</h2>;
}

function Garage() {
  return (
    <>
      <h1>Who lives in my Garage?</h1>
      <Car />
    </>
  );
}

ReactDOM.render(<Garage />, document.getElementById('root'));
```

## 파일 내부의 컴포넌트

React는 코드 재사용에 관한 것이므로 컴포넌트를 다른 파일로 분할하는 것이 좋습니다.

그러기 위해서는 ```.js``` 파일 확장자를 가진 새 파일을 만들고 그 안에 코드를 넣습니다.

{: .box-note}
파일명은 대문자로 시작해야 합니다.

###### 예제 6 - Car.js 파일 생성

```javascript
function Car() {
  return <h2>Hi, I am a Car!</h2>;
}

export default Car;
```

Car 구성 요소를 사용하려면 응용 프로그램에서 파일을 가져와야 합니다.

###### 예제 7 - "Car.js" 파일 import

```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import Car from './Car.js';

ReactDOM.render(<Car />, document.getElementById('root'));
```
