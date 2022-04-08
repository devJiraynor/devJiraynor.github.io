---
layout: post
title: JavaScript 26. 배열 반복 (Array Sort)
subtitle: 배열 반복 메서드는 모든 배열 항목에서 작동합니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 배열 반복

## 배열 forEach()

```forEach()``` 메서드는 각 배열 요소에 대해 함수(콜백 함수)를 한 번 호출합니다.

###### 예제 1

```javascript
const numbers = [45, 4, 9, 16, 25];
let txt = "";
numbers.forEach(myFunction);

function myFunction(value, index, array) {
  txt += value + "<br>";
}
```

함수는 세 개의 인수를 사용합니다.

+ 요소 값
+ 요소 인덱스
+ 배열 자체

위의 예에서는 값 매개 변수만 사용합니다. 이 예는 다음과 같이 다시 작성할 수 있습니다.

###### 예제 2

```javascript
const numbers = [45, 4, 9, 16, 25];
let txt = "";
numbers.forEach(myFunction);

function myFunction(value) {
  txt += value + "<br>";
}
```

## 배열 map()

```map()``` 메서드는 각 배열 요소에 대해 함수를 수행하여 새 배열을 만듭니다.

```map()``` 메서드는 값이 없는 배열 요소에 대해 함수를 실행하지 않습니다.

```map()``` 메서드는 원래 배열을 변경하지 않습니다.

이 예에서는 각 배열 값에 2를 곱합니다.

###### 예제 3

```javascript
const numbers1 = [45, 4, 9, 16, 25];
const numbers2 = numbers1.map(myFunction);

function myFunction(value, index, array) {
  return value * 2;
}
```

함수는 세 개의 인수를 사용합니다.

+ 요소 값
+ 요소 인덱스
+ 배열 자체

콜백 함수가 값 매개 변수만 사용하는 경우 인덱스 및 배열 매개 변수를 생략할 수 있습니다.

###### 예제 4

```javascript
const numbers1 = [45, 4, 9, 16, 25];
const numbers2 = numbers1.map(myFunction);

function myFunction(value) {
  return value * 2;
}
```

## 배열 filter()

```filter()``` 메서드는 테스트를 통과한 배열 요소를 사용하여 새 배열을 만듭니다.

다음 예제에서는 값이 18보다 큰 요소에서 새 배열을 생성합니다.

###### 예제 5

```javascript
const numbers = [45, 4, 9, 16, 25];
const over18 = numbers.filter(myFunction);

function myFunction(value, index, array) {
  return value > 18;
}
```

함수는 세 개의 인수를 사용합니다.

+ 요소 값
+ 요소 인덱스
+ 배열 자체

위의 예에서 콜백 함수는 인덱스 및 배열 매개 변수를 사용하지 않으므로 생략할 수 있습니다.

###### 예제 6

```javascript
const numbers = [45, 4, 9, 16, 25];
const over18 = numbers.filter(myFunction);

function myFunction(value) {
  return value > 18;
}
```

## 배열 reduce()

```reduce()``` 메서드는 각 배열 요소에 대해 함수를 실행하여 단일 값을 생성합니다.

```reduce()``` 메서드는 배열에서 왼쪽에서 오른쪽으로 작동합니다. ```reduceRight()```도 참조하십시오.

{: .box-note}
```reduce()``` 메서드는 원래 배열을 줄이지 않습니다.

다음 예제에서는 배열의 모든 숫자의 합을 찾습니다.

###### 예제 7

```javascript
const numbers = [45, 4, 9, 16, 25];
let sum = numbers.reduce(myFunction);

function myFunction(total, value, index, array) {
  return total + value;
}
```

함수는 4개의 인수를 사용합니다.

+ 총계(초기값/이전에 반환된 값)
+ 요소 값
+ 요소 색인
+ 배열 자체

위의 예에서는 인덱스 및 배열 매개 변수를 사용하지 않습니다. 다음과 같이 다시 쓸 수 있습니다.

###### 예제 8

```javascript
const numbers = [45, 4, 9, 16, 25];
let sum = numbers.reduce(myFunction);

function myFunction(total, value) {
  return total + value;
}
```

```reduce()``` 메서드는 다음과 같은 초기 값을 사용할 수 있습니다.

###### 예제 9

```javascript
const numbers = [45, 4, 9, 16, 25];
let sum = numbers.reduce(myFunction, 100);

function myFunction(total, value) {
  return total + value;
}
```

## 배열 reduceRight()

```reduceRight()``` 메서드는 각 배열 요소에 대해 함수를 실행하여 단일 값을 생성합니다.

```reduceRight()```는 배열에서 오른쪽에서 왼쪽으로 작동합니다.

{: .box-note}
```reduceRight()``` 메서드는 원래 배열을 줄이지 않습니다.

다음 예제에서는 배열의 모든 숫자의 합을 찾습니다.

###### 예제 10

```javascript
const numbers = [45, 4, 9, 16, 25];
let sum = numbers.reduceRight(myFunction);

function myFunction(total, value, index, array) {
  return total + value;
}
```

함수는 4개의 인수를 사용합니다.

+ 총계(초기값/이전에 반환된 값)
+ 요소 값
+ 요소 색인
+ 배열 자체

위의 예에서는 인덱스 및 배열 매개 변수를 사용하지 않습니다. 다음과 같이 다시 쓸 수 있다:

###### 예제 11

```javascript
const numbers = [45, 4, 9, 16, 25];
let sum = numbers.reduceRight(myFunction);

function myFunction(total, value) {
  return total + value;
}
```

## 배열 every()

```every()``` 메서드는 모든 배열 값이 테스트를 통과하는지 확인합니다.

이 예에서는 모든 배열 값이 18보다 큰지 확인합니다.

###### 예제 12

```javascript
const numbers = [45, 4, 9, 16, 25];
let allOver18 = numbers.every(myFunction);

function myFunction(value, index, array) {
  return value > 18;
}
```

함수는 세 개의 인수를 사용합니다.

+ 요소 값
+ 요소 색인
+ 배열 자체

콜백 함수가 첫 번째 파라미터(값)만 사용하는 경우 다른 파라미터는 생략할 수 있습니다.

###### 예제 13

```javascript
const numbers = [45, 4, 9, 16, 25];
let allOver18 = numbers.every(myFunction);

function myFunction(value) {
  return value > 18;
}
```

## 배열 some()

```some()``` 메서드는 일부 배열 값이 테스트를 통과하는지 확인합니다.

이 예에서는 일부 배열 값이 18보다 큰지 확인합니다.

###### 예제 14

```javascript
const numbers = [45, 4, 9, 16, 25];
let someOver18 = numbers.some(myFunction);

function myFunction(value, index, array) {
  return value > 18;
}
```

함수는 세 개의 인수를 사용합니다.

+ 요소 값
+ 요소 색인
+ 배열 자체

## 배열 indexOf()

```indexOf()``` 메서드는 배열에서 요소 값을 검색하고 위치를 반환합니다.

{: .box-note}
**Note:** 첫 번째 항목은 위치 0, 두 번째 항목은 위치는 1입니다.

###### 예제 15

```javascript
const fruits = ["Apple", "Orange", "Apple", "Mango"];
let position = fruits.indexOf("Apple") + 1;
```

#### 구문

```javascript
array.indexOf(item, start)
```

| item | 필수. 검색할 항목입니다. |
| start | 선택. 검색을 시작할 위치입니다. 음수 값은 지정된 위치 카운트에서 끝에서 시작하여 끝까지 검색합니다. |

```Array.indexOf()```는 항목을 찾을 수 없는 경우 -1을 반환합니다.

항목이 두 번 이상 있으면 첫 번째 항목의 위치를 반환합니다.

## 배열 lastIndexOf()

```Array.lastIndexOf()```은 ```Array.indexOf()```와 동일하지만 지정된 요소의 마지막 발생 위치를 반환합니다.

###### 예제 16

```javascript
const fruits = ["Apple", "Orange", "Apple", "Mango"];
let position = fruits.lastIndexOf("Apple") + 1;
```

#### 구문

```javascript
array.lastIndexOf(item, start)
```

| item | 필수. 검색할 항목 |
| start | 선택. 검색을 시작할 위치입니다. (음수 값일 경유 지정된 위치 카운트에서 끝에서 시작하여 검색 시작점까지) |

## 배열 find()

```find()``` 메서드는 테스트 함수를 통과한 첫 번째 배열 요소의 값을 반환합니다.

다음 예제에서는 18보다 큰 첫 번째 요소를 찾습니다(값을 반환합니다).

###### 예제 17

```javascript
const numbers = [4, 9, 16, 25, 29];
let first = numbers.find(myFunction);

function myFunction(value, index, array) {
  return value > 18;
}
```

함수는 세 개의 인수를 사용합니다.

+ 요소 값
+ 요소 색인
+ 배열 자체

#### 지원 브라우저

```find()```는 ES6 기능(JavaScript 2015)입니다.

모든 최신 브라우저에서 지원됩니다.

```find()```는 Internet Explorer에서 지원되지 않습니다.

## 배열 findIndex()

```findIndex()``` 메서드는 테스트 함수를 통과한 첫 번째 배열 요소의 인덱스를 반환합니다.

이 예에서는 18보다 큰 첫 번째 요소의 인덱스를 찾습니다.

###### 예제 18

```javascript
const numbers = [4, 9, 16, 25, 29];
let first = numbers.findIndex(myFunction);

function myFunction(value, index, array) {
  return value > 18;
}
```

함수는 세 개의 인수를 사용합니다.

+ 요소 값
+ 요소 색인
+ 배열 자체

#### 지원 브라우저

```findIndex()```는 ES6 기능입니다(JavaScript 2015).

모든 최신 브라우저에서 지원됩니다.

```findIndex()```는 Internet Explorer에서 지원되지 않습니다.

## Array.from()

```Array.from()``` 메서드는 ```length``` 속성 또는 반복 가능한 객체를 가진 객체에서 배열 객체를 반환합니다.

###### 예제 19

```javascript
Array.from("ABCDEFG");
```

#### 지원 브라우저

```from()```은 ES6 기능(JavaScript 2015)입니다.

모든 최신 브라우저에서 지원됩니다.

```from()```은 Internet Explorer에서 지원되지 않습니다.

## 배열 keys()

```Array.keys()``` 메서드는 배열 키가 있는 **ArrayIterator** 객체를 반환합니다.

###### 예제 20

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
const keys = fruits.keys();

for (let x of keys) {
  text += x + "<br>";
}
```

#### 지원 브라우저

```keys()```는 ES6 기능입니다(JavaScript 2015).

모든 최신 브라우저에서 지원됩니다.

```keys()```는 Internet Explorer에서 지원되지 않습니다.

## 배열 entries()

###### 예제 21 - 어레이 반복기를 생성한 다음 키/값 쌍을 반복합니다.

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
const f = fruits.entries();

for (let x of f) {
  document.getElementById("demo").innerHTML += x;
}
```

```entries()``` 메서드는 키/값 쌍이 있는 **ArrayIterator** 객체를 반환합니다.

[0, "Banana"]
[1, "Orange"]
[2, "Apple"]
[3, "Mango"]

```entries()``` 메서드는 원래 배열을 변경하지 않습니다.

#### 지원 브라우저

```entries()```는 ES6 기능입니다(JavaScript 2015).

모든 최신 브라우저에서 지원됩니다.

```entries()```은 Internet Explorer에서 지원되지 않습니다.

## 배열 includes()

ECMAScript 2016은 배열에 ```Array.includes()```를 도입했습니다. 이를 통해 배열(indexOf와 달리 NaN 포함)에 요소가 있는지 확인할 수 있습니다.

###### 예제 22

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];

fruits.includes("Mango"); // true
```

#### 구문

```javascript
array.includes(search-item)
```

{: .box-note}
```Array.includes()```를 사용하면 NaN 값을 확인할 수 있습니다. ```Array.indexOf()```와 다릅니다.

```Array.includes()```는 Internet Explorer 및 Edge 12/13에서 지원되지 않습니다.

완전히 지원되는 첫 번째 브라우저 버전은 다음과 같습니다.

#### 지원 브라우저

```includes()```는 ECMAScript 2016의 기능입니다.

모든 최신 브라우저에서 지원됩니다.

```includes()```는 Internet Explorer에서 지원되지 않습니다.
