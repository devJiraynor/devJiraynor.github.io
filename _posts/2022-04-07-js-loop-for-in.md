---
layout: post
title: JavaScript 39. for in 반복문 (For In Loop)
subtitle: 객체의 속성을 반복하는 for/in 반복에 대해 알아봅니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript for in 반복문

## for in 반복문

```for in``` 구문은 객체의 속성을 반복합니다.

#### 구문

```javascript
for (key in object) {
  // 실행할 코드 블록
}
```

###### 예제 1

```javascript
const person = {fname:"John", lname:"Doe", age:25};

let text = "";
for (let x in person) {
  text += person[x];
}
```

예제 설명:

+ **for in** 반복문은 **person** 객체에 대해 반복됩니다.
+ 각 반복은 **key** (x)를 반환합니다.
+ 키는 키의 **값**에 액세스하는 데 사용됩니다.
+ 키의 값은 **person[x]**입니다.

## 배열에 for in 사용

```for in``` 구문은 배열의 속성을 루프할 수도 있습니다.

#### 구문

```javascript
for (variable in array) {
  code
}
```

###### 예제 2

```javascript
const numbers = [45, 4, 9, 16, 25];

let txt = "";
for (let x in numbers) {
  txt += numbers[x];
}
```

{: .box-note}
인덱스 순서가 중요한 경우 ```for in```을 사용하지 마십시오.<br>인덱스 순서는 구현에 따라 다르며 배열 값에 원하는 순서대로 액세스하지 못할 수 있습니다.<br>순서가 중요한 경우에는 ```for``` 반복문, ```for of``` 반복문 또는 ```Array.forEach()```를 사용하는 것이 좋습니다.

## Array.forEach()

```forEach()``` 메서드는 각 배열 요소에 대해 함수(콜백 함수)를 한 번 호출합니다.

###### 예제 3

```javascript
const numbers = [45, 4, 9, 16, 25];

let txt = "";
numbers.forEach(myFunction);

function myFunction(value, index, array) {
  txt += value;
}
```

함수는 세 개의 인수를 사용합니다.

+ 요소 값
+ 요소 인덱스
+ 배열 자체

위의 예에서는 값 매개 변수만 사용합니다. 다음과 같이 다시 쓸 수 있습니다.

###### 예제 4

```javascript
const numbers = [45, 4, 9, 16, 25];

let txt = "";
numbers.forEach(myFunction);

function myFunction(value) {
  txt += value;
}
```
