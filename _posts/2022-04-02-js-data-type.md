---
layout: post
title: JavaScript 13. 데이터 타입 (Data Type)
subtitle: JavaScript 변수에는 숫자, 문자열, 개체 등의 다양한 데이터 유형을 포함할 수 있습니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 데이터 타입

## 데이터 타입의 개념

프로그래밍에서 데이터 타입은 중요한 개념입니다.

변수를 조작할 수 있으려면 타입에 대해 아는 것이 중요합니다.

데이터 타입이 없으면 컴퓨터가 아래 문제를 안전하게 해결할 수 없습니다.

```javascript
let x = 16 + "Volvo";
```

16에 "Volvo"를 추가하는 것은 말이되지 않습니다.

JavaScript는 위의 예를 다음과 같이 처리합니다.

```javascript
let x = "16" + "Volvo";
```

{: .box-note}
숫자와 문자열을 추가하면 JavaScript는 숫자를 문자열로 처리합니다.

###### 예제 1

```javascript
let x = 16 + "Volvo";
```

###### 예제 2

```javascript
let x = "Volvo" + 16;
```

JavaScript는 왼쪽에서 오른쪽으로 식을 평가합니다. 순서가 다르면 다음과 같은 결과가 나올 수 있습니다.

###### 예제 3

```javascript
let x = 16 + 4 + "Volvo";
```

결과 :

<samp>20Volvo</samp>

###### 예제 4

```javascript
let x = "Volvo" + 16 + 4;
```

결과 : 

<samp>Volvo164</samp>

첫 번째 예에서 JavaScript는 "Volvo"에 도달할 때까지 16과 4를 숫자로 처리합니다.

두 번째 예에서는 첫 번째 피연산자가 문자열이기 때문에 모든 피연산자가 문자열로 취급됩니다.

## 타입의 역동성

JavaScript에는 동적 타입이 있습니다. 즉, 동일한 변수를 사용하여 다른 데이터 타입을 유지할 수 있습니다.

###### 예제 5

```javascript
let x;           // x : undefined
x = 5;           // x : Number
x = "John";      // x : String
```

## 문자열

문자열(또는 텍스트 문자열)은 "John Doe"와 같은 일련의 문자입니다.

문자열은 따옴표로 작성됩니다. 작은따옴표 또는 큰따옴표를 사용할 수 있습니다.

###### 예제 6

```javascript
let carName1 = "Volvo XC60";
let carName2 = 'Volvo XC60';
```

문자열을 둘러싼 따옴표와 일치하지 않는 한 문자열 내부에 따옴표를 사용할 수 있습니다.

###### 예제 7

```javascript
let answer1 = "It's alright";             // 큰 따옴표 안의 작은 따옴표
let answer2 = "He is called 'Johnny'";    // 큰 따옴표 안의 작은 따옴표
let answer3 = 'He is called "Johnny"';    // 작은 따옴표 안의 큰 따옴표
```

## 숫자

JavaScript에는 한 가지 유형의 숫자만 있습니다.

숫자는 소수점 또는 소수점 없이 쓸 수 있습니다.

###### 예제 8

```javascript
let x1 = 34.00;     // 소수점 사용
let x2 = 34;        // 소수점 미사용
```

큰 숫자 또는 작은 숫자를 지수 표기로 쓸 수 있습니다.

###### 예제 9

```javascript
let y = 123e5;      // 12300000
let z = 123e-5;     // 0.00123
```

## 불린

불린에는 ```true``` 또는 ```false```의 두 가지 값만 사용할 수 있습니다.

###### 예제 10

```javascript
let x = 5;
let y = 5;
let z = 6;
(x == y)       // Returns true
(x == z)       // Returns false
```

불린은 종종 조건부 테스트에 사용됩니다.

## 배열

JavaScript 배열은 대괄호(```[]```)로 작성됩니다.

배열 항목은 쉼표로 구분됩니다.

다음 코드는 세 가지 항목(차량 이름)을 포함하는 ```cars```라는 배열을 선언합니다.

###### 예제 11

```javascript
const cars = ["Saab", "Volvo", "BMW"];
```

배열 인덱스는 0을 기반으로 합니다. 즉, 첫 번째 항목은 ```[0]```이고 두 번째 항목은 ```[1]```입니다.

## 객체

JavaScript 객체는 중괄호(```{}```)로 작성됩니다.

객체 속성은 쉼표로 구분된 name:value 쌍으로 작성됩니다.

###### 예제 12

```javascript
const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```

위의 예에서 객체(```person```)에는 ```firstName```, ```lastName```, ```age```, ```eyeColor```의 4가지 속성이 있습니다.

## typeof 연산자

JavaScript ```typeof``` 연산자를 사용하여 JavaScript 변수의 타입을 찾을 수 있습니다.

```typeof``` 연산자는 타입을 반환합니다.

###### 예제 13

```javascript
typeof ""             // Returns "string"
typeof "John"         // Returns "string"
typeof "John Doe"     // Returns "string"
```

###### 예제 14

```javascript
typeof 0              // Returns "number"
typeof 314            // Returns "number"
typeof 3.14           // Returns "number"
typeof (3)            // Returns "number"
typeof (3 + 4)        // Returns "number"
```

## undefined

JavaScript에서 값이 없는 변수는 값을 ```undefined```라고 합니다. 타입 또한 ```undefined```입니다.

###### 예제 15

```javascript
let car;    // 값 : undefined, 타입 : undefined
```

값을 ```undefined```으로 설정하면 변수를 비울 수 있습니다. 타입 또한 ```undefined```입니다.

###### 예제 16

```javascript
car = undefined;    // 값 : undefined, 타입 : undefined
```

## 빈 값

빈 값은 ```undefined```하고는 다릅니다.

빈 문자열에는 값과 타입이 모두 존재합니다.

###### 예제 17

```javascript
let car = "";    // 값 : "", 타입 : "string"
```
