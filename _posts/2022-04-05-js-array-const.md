---
layout: post
title: JavaScript 27. 배열 Const (Array Const)
subtitle: ES6 부터는 배열을 선언할 시 const를 사용하는 것이 일반적입니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 배열 Const

## ECMAScript 2015 (ES6)

2015년 자바스크립트는 중요한 새로운 키워드인 ```const```를 도입하였습니다.

```const```를 사용하여 배열을 선언하는 것이 일반적인 관례가 되었습니다.

###### 예제 1

```javascript
const cars = ["Saab", "Volvo", "BMW"];
```

## 재할당 불가

```const```로 선언된 배열은 재할당할 수 없습니다.

###### 예제 2

```javascript
const cars = ["Saab", "Volvo", "BMW"];
cars = ["Toyota", "Volvo", "Audi"];    // ERROR
```

## 배열은 상수가 아님

```const```라는 키워드는 약간 오해의 소지가 있습니다.

상수 배열을 정의하는 것이 아닙니다. 배열에 대한 지속적인 참조를 정의합니다.

이 때문에 상수 배열의 요소를 변경할 수 있습니다.

## 요소는 재할당 가능

상수 배열의 요소를 변경할 수 있습니다.

###### 예제 3

```javascript
// 상수 배열을 생성할 수 있습니다.
const cars = ["Saab", "Volvo", "BMW"];

// 요소를 변경할 수 있습니다.
cars[0] = "Toyota";

// 요소를 추가할 수 있습니다.
cars.push("Audi");
```

## 지원 브라우저

Internet Explorer 10 이전 버전에서는 ```const``` 키워드가 지원되지 않습니다.

다음 표에서는 ```const``` 키워드를 완전히 지원하는 첫 번째 브라우저 버전을 정의합니다.

| **브라우저** | 구글 Chrome | 마이크로소프트 Edge | Firefox | Safari | Opera |
| **버전** | 49 | 11 | 36 | 10 | 36 |

## 선언할 때 할당됨

JavaScript ```const``` 변수에는 선언된 값이 할당되어야 합니다.

의미: ```const```로 선언된 배열을 선언할 때 초기화해야 합니다.

배열을 초기화하지 않고 ```const```를 사용하면 구문 오류가 발생합니다.

###### 예제 4

```javascript
const cars;
cars = ["Saab", "Volvo", "BMW"];  // ERROR
```

```var```로 선언된 배열은 언제든지 초기화할 수 있습니다.

배열을 선언하기 전에 사용할 수도 있습니다.

###### 예제 5

```javascript
cars = ["Saab", "Volvo", "BMW"];
var cars;
```

## Const 블록 범위

```const```로 선언된 배열에 **Block Scope**가 있습니다.

블록에서 선언된 배열은 블록 외부에 선언된 배열과 다릅니다.

###### 예제 5

```javascript
const cars = ["Saab", "Volvo", "BMW"];
// 여기서 cars[0] : Saab
{
  const cars = ["Toyota", "Volvo", "BMW"];
  // 여기서 cars[0] : Toyota
}
// 여기서 cars[0] : "Saab"
```

```var```로 선언된 배열은 블록 범위가 없습니다.

###### 예제 6

```javascript
var cars = ["Saab", "Volvo", "BMW"];
// 여기서 cars[0] : "Saab"
{
  var cars = ["Toyota", "Volvo", "BMW"];
  // 여기서 cars[0] : "Toyota"
}
// 여기서 cars[0] : "Toyota"
```

## 배열 재할당

```var```로 선언된 배열을 다시 선언할 수 있는 프로그램

###### 예제 7

```javascript
var cars = ["Volvo", "BMW"];   // 가능
var cars = ["Toyota", "BMW"];  // 가능
cars = ["Volvo", "Saab"];      // 가능
```

```const```로 선언된 배열은 동일한 범위 또는 동일한 블록에서 다시 지우거나 재할당할 수 없습니다.

###### 예제 8

```javascript
var cars = ["Volvo", "BMW"];     // 가능
const cars = ["Volvo", "BMW"];   // 불가능
{
  var cars = ["Volvo", "BMW"];   // 가능
  const cars = ["Volvo", "BMW"]; // 불가능
}
```

동일한 범위 또는 동일한 블록에서 기존 ```const```로 선언된 배열을 다시 선언하거나 재할당할 수 없습니다.

###### 예제 9

```javascript
const cars = ["Volvo", "BMW"];   // 가능
const cars = ["Volvo", "BMW"];   // 불가능
var cars = ["Volvo", "BMW"];     // 불가능
cars = ["Volvo", "BMW"];         // 불가능

{
  const cars = ["Volvo", "BMW"]; // 가능
  const cars = ["Volvo", "BMW"]; // 불가능
  var cars = ["Volvo", "BMW"];   // 불가능
  cars = ["Volvo", "BMW"];       // 불가능
}
```

다른 범위 또는 다른 블록에서 ```const```를 사용하여 배열을 다시 선언할 수 있습니다.

###### 예제 10

```javascript
const cars = ["Volvo", "BMW"];   // 가능
{
  const cars = ["Volvo", "BMW"]; // 가능
}
{
  const cars = ["Volvo", "BMW"]; // 가능
}
```
