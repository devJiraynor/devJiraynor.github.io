---
layout: post
title: React 07. 클래스 컴포넌트 (Class Components)
subtitle: React 16.8 이전에는 Class 컴포넌트가 React 컴포넌트의 상태와 라이프 사이클을 추적할 수 있는 유일한 방법이었습니다. 함수 컴포넌트는 "state-less"로 간주되었습니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React 클래스 컴포넌트

React 16.8 이전에는 Class 컴포넌트가 React 컴포넌트의 상태와 라이프 사이클을 추적할 수 있는 유일한 방법이었습니다. 함수 컴포넌트는 "state-less"로 간주되었습니다.

후크가 추가되어 함수 컴포넌트는 클래스 컴포넌트와 거의 동일합니다. 차이는 매우 작기 때문에 React에서 Class 컴포넌트를 사용할 필요가 없습니다.

함수 컴포넌트 요소를 선호하지만, 현재 React에서 클래스 컴포넌트를 제거할 계획은 없습니다.

이 섹션에서는 React에서 클래스 컴포넌트를 사용하는 방법에 대한 개요를 제공합니다.

## React 컴포넌트

컴포넌트는 독립된 재사용 가능한 코드 비트입니다. 이들은 JavaScript 함수와 동일한 목적을 수행하지만 단독으로 작동하며 ```render()``` 함수를 통해 HTML을 반환합니다.

컴포넌트는 클래스 컴포넌트와 함수 컴포넌트의 2가지 타입이 있습니다.이 장에서는 클래스 컴포넌트에 대해 설명합니다.

## 클래스 컴포넌트 생성

React 구성 요소를 생성할 때 구성 요소 이름은 대문자로 시작해야 합니다.

구성 요소는 ```extends React.Component``` 문을 포함해야 하며, 이 문은 ```React.Component```에 대한 상속을 생성하고 구성 요소에 ```React.Component``` 함수에 대한 액세스 권한을 부여합니다.

컴포넌트에는 render() 메서드도 필요합니다.이 메서드는 HTML을 반환합니다.

###### 예제 1 - Car 클래스 컴포넌트 생성

```javascript
class Car extends React.Component {
  render() {
    return <h2>Hi, I am a Car!</h2>;
  }
}
```

React 어플리케이션에는 ```<h2>``` 요소를 반환하는 Car라는 컴포넌트가 있습니다.

응용 프로그램에서 이 컴포넌트를 사용하려면 일반 HTML과 동일한 구문을 사용합니다. ```< Car />```

###### 예제 2 - Car 컴포넌트를 root에 출력

```javascript
ReactDOM.render(<Car />, document.getElementById('root'));
```

## 컴포넌트 생성자

컴포넌트에 ```constructor()``` 함수가 있는 경우 컴포넌트가 시작되면 이 함수가 호출됩니다.

생성자 함수는 구성 요소의 속성을 시작하는 위치입니다.

React에서 컴포넌트 속성은 ```state``` 라는 오브젝트로 유지되어야 합니다.

또한 컨스트럭터 함수는 부모 컴포넌트의 컨스트럭터 함수를 실행하는 ```super()``` 문을 포함하여 부모 컴포넌트의 상속을 보증하고 컴포넌트는 부모 컴포넌트의 모든 함수에 액세스할 수 있습니다(React.Component).

###### 예제 3 - Car 구성요소에 생성자 함수를 만들고 color 특성을 추가

```javascript
class Car extends React.Component {
  constructor() {
    super();
    this.state = {color: "red"};
  }
  render() {
    return <h2>I am a Car!</h2>;
  }
}
```

```render()``` 함수의 ```color``` 속성을 사용합니다.

```javascript
class Car extends React.Component {
  constructor() {
    super();
    this.state = {color: "red"};
  }
  render() {
    return <h2>I am a {this.state.color} Car!</h2>;
  }
}
```

## Props

컴포넌트 특성을 처리하는 또 다른 방법은 ```props```를 사용하는 것입니다.

```props```는 함수의 파라미터와 같으며, 속성으로 컴포넌트에 보냅니다.

###### 예제 4 - 속성을 사용하여 color를 Car 컴포넌트에 전달하고 render() 함수로 사용

```javascript
class Car extends React.Component {
  render() {
    return <h2>I am a {this.props.color} Car!</h2>;
  }
}

ReactDOM.render(<Car color="red"/>, document.getElementById('root'));
```

## 생성자에서의 Props

컴포넌트에 컨스트럭터 함수가 있는 경우 props는 항상 ```super()``` 메서드를 통해 컨스트럭터 및 React.Component에 전달됩니다.

```javascript
class Car extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return <h2>I am a {this.props.model}!</h2>;
  }
}

ReactDOM.render(<Car model="Mustang"/>, document.getElementById('root'));
```

## 컴포넌트 안에서 컴포넌트 사용

다른 컴포넌트 내부의 컴포넌트를 참조할 수 있습니다.

###### 예제 5 - Garage 구성 요소 내에서 Car 구성 요소를 사용

```javascript
class Car extends React.Component {
  render() {
    return <h2>I am a Car!</h2>;
  }
}

class Garage extends React.Component {
  render() {
    return (
      <div>
      <h1>Who lives in my Garage?</h1>
      <Car />
      </div>
    );
  }
}

ReactDOM.render(<Garage />, document.getElementById('root'));
```

## 파일 안에서 컴포넌트 사용

React는 코드를 재사용하는 것입니다. 또한 컴포넌트의 일부를 다른 파일에 삽입하는 것이 현명할 수 있습니다.

그러기 위해서는 ```.js``` 파일 확장자를 가진 새 파일을 만들고 그 안에 코드를 넣습니다.

파일은 이전과 같이 React를 Import하여 ```export default Car;``` 로 종료해야 합니다.

###### 예제 6 - Car.js 생성

```javascript
import React from 'react';

class Car extends React.Component {
  render() {
    return <h2>Hi, I am a Car!</h2>;
  }
}

export default Car;
```

```Car``` 구성 요소를 사용하려면 응용 프로그램에서 파일을 가져와야 합니다.

###### 예제 7 - 이제 응용 프로그램에 ```Car.js``` 파일을 Import합니다. ```Car``` 컴포넌트를 여기서 작성한 것처럼 사용할 수 있습니다.

```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import Car from './Car.js';

ReactDOM.render(<Car />, document.getElementById('root'));
```

## 클래스 컴포넌트 state

React Class 구성 요소에는 기본 제공 ```state``` 개체가 있습니다.

컴포넌트 컨스트럭터 섹션에서 ```state``` 를 사용한 적이 있습니다.

```state``` 개체는 구성 요소에 속하는 속성 값을 저장하는 위치입니다.

```state``` 개체가 변경되면 구성 요소가 다시 렌더링됩니다.

## state 객체 생성

```state``` 객체는 생성자에서 초기화됩니다.

###### 예제 8 - 생성자 메서드에서 state 객체를 지정합니다.

```javascript
class Car extends React.Component {
  constructor(props) {
    super(props);
    this.state = {brand: "Ford"};
  }
  render() {
    return (
      <div>
        <h1>My Car</h1>
      </div>
    );
  }
}
```

state 객체에는 원하는 개수의 속성을 포함할 수 있습니다.

###### 예제 9 - 컴포넌트에 필요한 모든 속성을 지정

```javascript
class Car extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      brand: "Ford",
      model: "Mustang",
      color: "red",
      year: 1964
    };
  }
  render() {
    return (
      <div>
        <h1>My Car</h1>
      </div>
    );
  }
}
```

## ```state``` 객체 사용

```this.state.propertyname``` 구문을 사용하여 컴포넌트 내의 임의의 ```state``` 객체를 참조합니다.

###### 예제 10 - ```render()``` 메서드의 ```state``` 객체를 참조

```javascript
class Car extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      brand: "Ford",
      model: "Mustang",
      color: "red",
      year: 1964
    };
  }
  render() {
    return (
      <div>
        <h1>My {this.state.brand}</h1>
        <p>
          It is a {this.state.color}
          {this.state.model}
          from {this.state.year}.
        </p>
      </div>
    );
  }
}
```

## ```state``` 객체 변경

state 객체의 값을 변경하려면 ```this.setState()``` 메서드를 사용합니다.

```state``` 객체의 값이 변경되면 컴포넌트가 다시 렌더링되므로 출력이 새 값에 따라 변경됩니다.

###### 예제 11 - color 속성을 변경하는 ```onClick``` 이벤트가 있는 버튼을 추가

```javascript
class Car extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      brand: "Ford",
      model: "Mustang",
      color: "red",
      year: 1964
    };
  }
  changeColor = () => {
    this.setState({color: "blue"});
  }
  render() {
    return (
      <div>
        <h1>My {this.state.brand}</h1>
        <p>
          It is a {this.state.color}
          {this.state.model}
          from {this.state.year}.
        </p>
        <button
          type="button"
          onClick={this.changeColor}
        >Change color</button>
      </div>
    );
  }
}
```

{: .box-note}
항상 ```setState()``` 메서드를 사용하여 상태 객체를 변경해 주세요. 이 메서드는 컴포넌트가 갱신되었음을 인식하고 ```render()``` 메서드(및 기타 모든 라이프 사이클 메서드)를 호출합니다.

## 컴포넌트의 생명주기

React의 각 구성 요소에는 3가지 주요 단계에서 모니터링 및 조작할 수 있는 라이프 사이클이 있습니다.

**Mounting**, **Updating**, **Unmounting** 3가지 단계가 있습니다.

## Mounting

Mounting이란 요소를 DOM에 넣는 것을 의미합니다.

React에는 컴포넌트를 마운트할 때 다음 순서로 호출되는 4가지 메서드가 내장되어 있습니다.

1. ```constructor()```
2. ```getDerivedStateFromProps()```
3. ```render()```
4. ```componentDidMount()```

```render()``` 메서드는 필수이며 항상 호출됩니다. 다른 메서드는 옵션이며 정의하면 호출됩니다.

#### constructor

```constructor()``` 메서드는 컴포넌트가 시작되었을 때 가장 먼저 호출되며 초기 ```state``` 및 기타 초기 값을 설정하는 함수입니다.

```constructor()``` 메서드는 인수로서 ```props```와 함께 호출되며, 항상 먼저 ```super(props)```를 호출해야 합니다.이것에 의해 부모(```React.Component```) 컨스트럭터 메서드가 개시되어 컴포넌트가 부모로부터 메서드를 상속받을 수 있습니다.

###### 예제 12 - 컴포넌트를 만들 때마다 React에 의해 ```constructor``` 함수가 호출됨

```javascript
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  render() {
    return (
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));
```

#### getDerivedStateFromProps

```getDerivedStateFromProps()``` 메서드는 DOM 내의 요소를 렌더링하기 직전에 호출됩니다.

초기 ```props```를 기준으로 ```state``` 객체를 설정하는 함수입니다.

이 명령어는 ```state```를 인수로 사용하고 ```state```를 변경한 객체를 반환합니다.

다음 예시는 ```favoritecolor```가 "red"인 상태에서 시작하지만 ```getDerivedStateFromProps()``` 메서드는 ```favcol``` 속성을 기반으로 ```favoritecolor```를 업데이트합니다.

###### 예제 13 - ```getDerivedStateFromProps()``` 메서드는 ```render()``` 메서드 직전에 호출됨

```javascript
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  static getDerivedStateFromProps(props, state) {
    return {favoritecolor: props.favcol };
  }
  render() {
    return (
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
    );
  }
}

ReactDOM.render(<Header favcol="yellow"/>, document.getElementById('root'));
```

#### render

```render()``` 메서드는 필수이며 실제로 HTML을 DOM에 출력하는 메서드입니다.

###### 예제 14 - ```render()``` 메서드를 사용하는 단순한 컴포넌트

```javascript
class Header extends React.Component {
  render() {
    return (
      <h1>This is the content of the Header component</h1>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));
```

#### componentDidMount

componentDidMount() 메서드는 컴포넌트가 렌더링된 후에 호출됩니다.

여기서 컴포넌트가 DOM에 배치된 후 실행되어야 하는 구문을 실행합니다.

###### 예제 15 - 처음 ```favoritecolor```는 "red"였지만 1초 후 "yellow"로 변경됨

```javascript
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  componentDidMount() {
    setTimeout(() => {
      this.setState({favoritecolor: "yellow"})
    }, 1000)
  }
  render() {
    return (
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));
```

## Updating

라이프 사이클의 다음 단계는 컴포넌트가 갱신되는 시점입니다.

컴포넌트는 컴포넌트 ```state``` 또는 ```props```가 변경될 때마다 갱신됩니다.

React에는 컴포넌트가 갱신되면 다음 순서로 호출되는 5가지 메서드가 내장되어 있습니다.

1. ```getDerivedStateFromProps()```
2. ```shouldComponentUpdate()```
3. ```render()```
4. ```getSnapshotBeforeUpdate()```
5. ```componentDidUpdate()```

```render()``` 메서드는 필수이며 항상 호출됩니다. 다른 메서드는 옵션이며 정의하면 호출됩니다.

#### getDerivedStateFromProps

업데이트 시 ```getDerivedStateFromProps()``` 메서드가 호출됩니다. 이것은 컴포넌트가 갱신될 때 호출되는 첫 번째 메서드입니다.

초기 ```props```를 바탕으로 ```state``` 객체를 설정할 수 있는 함수입니다.

다음 예에서는 ```favoritecolor```을 "blue"으로 변경하는 버튼이 있는데, ```getDerivedStateFromProps()``` 메서드가 호출되어 ```favcol``` 속성의 색상으로 상태가 업데이트되므로 ```favoritecolor```는 "yellow"로 계속 렌더링됩니다.

###### 예제 16 - 컴포넌트가 갱신되면 ```getDerivedStateFromProps()``` 메서드는 다음과 같이 호출됨

```javascript
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  static getDerivedStateFromProps(props, state) {
    return {favoritecolor: props.favcol };
  }
  changeColor = () => {
    this.setState({favoritecolor: "blue"});
  }
  render() {
    return (
      <div>
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
      <button type="button" onClick={this.changeColor}>Change color</button>
      </div>
    );
  }
}

ReactDOM.render(<Header favcol="yellow"/>, document.getElementById('root'));
```

#### shouldComponentUpdate

```showComponentUpdate()``` 메서드에서는 React가 렌더링을 계속할 것인지 여부를 지정하는 논리 값을 반환할 수 있습니다.

기본값은 ```true``` 입니다.

다음 예시는 ```shouldComponentUpdate()``` 메서드가 ```false``` 를 반환했을 때 어떻게 되는지 보여 줍니다.

###### 예제 17 - 업데이트 시 구성 요소의 렌더링을 중지함

```javascript
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  shouldComponentUpdate() {
    return false;
  }
  changeColor = () => {
    this.setState({favoritecolor: "blue"});
  }
  render() {
    return (
      <div>
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
      <button type="button" onClick={this.changeColor}>Change color</button>
      </div>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));
```

###### 예제 18 - ```shouldComponentUpdate()``` 메서드가 ```true``` 를 반환

```javascript
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  shouldComponentUpdate() {
    return true;
  }
  changeColor = () => {
    this.setState({favoritecolor: "blue"});
  }
  render() {
    return (
      <div>
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
      <button type="button" onClick={this.changeColor}>Change color</button>
      </div>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));
```

#### render

```render()``` 메서드는 컴포넌트가 갱신되면 당연히 호출됩니다. 이 메서드는 새로운 변경이 발생하면 HTML을 DOM으로 다시 렌더링 합니다.

다음 예에서는 ```favoritecolor```을 "blue"로 변경하는 버튼이 있습니다.

###### 예제 19 - 버튼을 클릭하여 컴포넌트 상태를 변경

```javascript
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  changeColor = () => {
    this.setState({favoritecolor: "blue"});
  }
  render() {
    return (
      <div>
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
      <button type="button" onClick={this.changeColor}>Change color</button>
      </div>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));
```

#### getSnapshotBeforeUpdate

```getSnapshotBeforeUpdate()``` 메서드에서는 업데이트 전 ```props``` 및 ```state```에 액세스할 수 있습니다. 즉, 업데이트 후에도 업데이트 전 값을 확인할 수 있습니다.

```getSnapshotBeforeUpdate()``` 메서드가 있는 경우 ```componentDidUpdate()``` 메서드도 포함해야 합니다. 그렇지 않으면 오류가 발생합니다.

다음 예시는 복잡해 보일 수 있지만 이 예에서는 다음과 같은 기능만 수행합니다.

컴포넌트가 마운트되면, ```favoritecolor``` 는 "red" 로 렌더링 됩니다.

컴포넌트가 마운트되면 타이머에 의해 ```state```가 변화하고 1초 후에 ```favoritecolor```가 "yellow"가 됩니다.

이 액션은 업데이트 단계를 트리거합니다. 이 컴포넌트는 ```getSnapshotBeforeUpdate()``` 메서드를 가지고 있기 때문에 이 메서드가 실행되어 빈 DIV1 요소에 메시지가 기록됩니다.

그런 다음 ```componentDidUpdate()``` 메서드가 실행되어 빈 DIV2 요소에 메시지가 기록됩니다.

###### 예제 20 - ```getSnapshotBeforeUpdate()``` 메서드를 사용하여 업데이트 전 상태 개체를 확인

```javascript
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  componentDidMount() {
    setTimeout(() => {
      this.setState({favoritecolor: "yellow"})
    }, 1000)
  }
  getSnapshotBeforeUpdate(prevProps, prevState) {
    document.getElementById("div1").innerHTML =
    "Before the update, the favorite was " + prevState.favoritecolor;
  }
  componentDidUpdate() {
    document.getElementById("div2").innerHTML =
    "The updated favorite is " + this.state.favoritecolor;
  }
  render() {
    return (
      <div>
        <h1>My Favorite Color is {this.state.favoritecolor}</h1>
        <div id="div1"></div>
        <div id="div2"></div>
      </div>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));
```

#### componentDidUpdate

```componentDidUpdate``` 메서드는 DOM에서 구성 요소가 업데이트된 후 호출됩니다.

다음 예시는 복잡해 보일 수 있지만 이 예에서는 다음과 같은 기능만 수행합니다.

컴포넌트가 마운트되면, ```favoritecolor```는 "red" 로 렌더링 됩니다.

컴포넌트가 마운트되면 타이머에 의해 ```state```가 변화하고 ```favoritecolor``` "yellow" 됩니다.

이 액션은 업데이트 단계를 트리거합니다. 이 컴포넌트에는 ```componentDidUpdate``` 메서드가 있기 때문에 다음 메서드가 실행되어 빈 DIV 요소에 메시지가 기록됩니다.

###### 예제 21 - ```componentDidUpdate``` 메서드는 업데이트가 DOM에 렌더링된 후 호출됨

```javascript
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  componentDidMount() {
    setTimeout(() => {
      this.setState({favoritecolor: "yellow"})
    }, 1000)
  }
  componentDidUpdate() {
    document.getElementById("mydiv").innerHTML =
    "The updated favorite is " + this.state.favoritecolor;
  }
  render() {
    return (
      <div>
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
      <div id="mydiv"></div>
      </div>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));
```

## Unmounting

라이프 사이클의 다음 단계는 구성 요소가 DOM에서 제거되거나 React가 원하는 대로 마운트 해제하는 것입니다.

React에는 컴포넌트가 마운트 해제되었을 때 호출되는 메서드가 1개밖에 없습니다.

+ ```componentWillUnmount()```

#### componentWillUnmount

```componentWillUnmount``` 메서드는 컴포넌트가 DOM에서 삭제될 때 호출됩니다.

###### 예제 22 - 버튼을 클릭하여 헤더를 삭제

```javascript
class Container extends React.Component {
  constructor(props) {
    super(props);
    this.state = {show: true};
  }
  delHeader = () => {
    this.setState({show: false});
  }
  render() {
    let myheader;
    if (this.state.show) {
      myheader = <Child />;
    };
    return (
      <div>
      {myheader}
      <button type="button" onClick={this.delHeader}>Delete Header</button>
      </div>
    );
  }
}

class Child extends React.Component {
  componentWillUnmount() {
    alert("The component named Header is about to be unmounted.");
  }
  render() {
    return (
      <h1>Hello World!</h1>
    );
  }
}

ReactDOM.render(<Container />, document.getElementById('root'));
```
