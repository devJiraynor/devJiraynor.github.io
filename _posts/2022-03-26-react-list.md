---
layout: post
title: React 11. 리스트 (Lists)
subtitle: 리액트에서는 루프 타입이 있는 리스트를 렌더링합니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React 리스트

## React 리스트

리액트에서는 루프 타입이 있는 리스트를 렌더링합니다.

일반적으로 JavaScript ```map()``` 배열 방식이 선호됩니다.

###### 예제 1 - Garage에 있는 모든 Car를 렌더링합니다.

```javascript
function Car(props) {
  return <li>I am a { props.brand }</li>;
}

function Garage() {
  const cars = ['Ford', 'BMW', 'Audi'];
  return (
    <>
      <h1>Who lives in my garage?</h1>
      <ul>
        {cars.map((car) => <Car brand={car} />)}
      </ul>
    </>
  );
}

ReactDOM.render(<Garage />, document.getElementById('root'));
```

단, ```create-react-app```에서 이 코드를 실행하면 동작하지만 목록 항목에 대해 제공된 "key"가 없다는 경고가 표시됩니다.

## Keys

키를 사용하면 React가 요소를 추적할 수 있습니다. 이렇게 하면 항목이 업데이트되거나 제거되면 전체 목록이 아니라 해당 항목만 다시 렌더링됩니다.

키는 각 요소에서 고유해야 합니다. 그러나 글로벌하게 복제될 수 있습니다.

{: .box-note}
일반적으로 키는 각 항목에 할당된 고유 ID여야 합니다. 마지막 수단으로 배열 인덱스를 키로 사용할 수 있습니다.

###### 예제 2 - 이전 예에서 키를 포함하도록 리팩토링해 보겠습니다.

```javascript
function Car(props) {
  return <li>I am a { props.brand }</li>;
}

function Garage() {
  const cars = [
    {id: 1, brand: 'Ford'},
    {id: 2, brand: 'BMW'},
    {id: 3, brand: 'Audi'}
  ];
  return (
    <>
      <h1>Who lives in my garage?</h1>
      <ul>
        {cars.map((car) => <Car key={car.id} brand={car.brand} />)}
      </ul>
    </>
  );
}

ReactDOM.render(<Garage />, document.getElementById('root'));
```
