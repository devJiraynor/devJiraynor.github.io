---
layout: post
title: JavaScript 24. 배열 메서드 (Array Method)
subtitle: 배열 메서드들에 대해서 알아봅니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 배열 메서드

## 배열을 문자열로 변환

```toString()```로 변환하는 JavaScript 메서드는 배열을 쉼표로 구분된 배열 값의 문자열로 변환합니다.

###### 예제 1

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.toString();
```

또한 ```join()``` 메서드는 모든 배열 요소를 문자열로 결합합니다.

```toString()```과 동일하게 동작하지만 다음과 같이 구분자를 지정할 수 있습니다.

###### 예제 2

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.join(" * ");
```

## Popping 과 Pushing

배열로 작업할 때 요소를 제거하고 새 요소를 추가하는 것이 쉽습니다.

이것이 바로 터지고 밀리는 것입니다.

배열에서 항목을 **꺼내거나** 배열로 항목을 **밀어넣습니다.**

## 배열 pop()

```pop()``` 메서드는 배열에서 마지막 요소를 제거합니다.

###### 예제 3

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.pop();
```

```pop()``` 메서드는 "팝아웃"된 값을 반환합니다.

## 배열 push()

```push()``` 메서드는 배열(마지막)에 새 요소를 추가합니다.

###### 예제 4

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.push("Kiwi");
```

```push()``` 메서드는 새 배열 길이를 반환합니다.

###### 예제 5

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let length = fruits.push("Kiwi");
```

## 요소 변경

시프트는 팝핑과 동일하지만 마지막 요소 대신 첫 번째 요소를 작업합니다.

## 배열 shift()

```shift()``` 메서드는 첫 번째 배열 요소를 제거하고 다른 모든 요소를 하위 인덱스로 "전환"합니다.

###### 예제 6

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.shift();
```

```shift()``` 메서드는 "시프트 아웃" 값을 반환합니다.

###### 예제 7

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits.shift();
```

## 배열 unshift()

```unshift()``` 메서드는 배열에 새 요소를 추가하고(처음에) 이전 요소를 "시프트 해제"합니다.

###### 예제 8

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.unshift("Lemon");
```

## 요소 변경

배열 요소는 **인덱스 번호**를 사용하여 액세스됩니다.

{: .box-note}
배열 인덱스는 0으로 시작합니다.<br>[0] 첫 번째 배열 요소입니다.<br>[1] 두 번째입니다.<br>[2] 세 번째...

###### 예제 9

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[0] = "Kiwi";
```

## 배열 length

```length``` 속성을 사용하면 새 요소를 배열에 쉽게 추가할 수 있습니다.

###### 예제 10

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[fruits.length] = "Kiwi";
```

## 배열 delete()

{: .box-danger}
배열 요소는 JavaScript 연산자 ```delete```를 사용하여 삭제할 수 있습니다.<br>```delete```를 사용하면 배열에 ```undefined``` 구멍이 남습니다.<br>대신 pop() 또는 shift()를 사용합니다.

###### 예제 11

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
delete fruits[0];
```

## 배열 병합(연결)

```concat()``` 메서드는 기존 배열을 병합(연결)하여 새 배열을 생성합니다.

###### 예제 12

```javascript
const myGirls = ["Cecilie", "Lone"];
const myBoys = ["Emil", "Tobias", "Linus"];

const myChildren = myGirls.concat(myBoys);
```

{: .box-note}
```concat()``` 메서드는 기존 배열을 변경하지 않습니다. 항상 새 배열을 반환합니다.

```concat()``` 메서드는 임의의 수의 배열 인수를 사용할 수 있습니다.

###### 예제 13

```javascript
const arr1 = ["Cecilie", "Lone"];
const arr2 = ["Emil", "Tobias", "Linus"];
const arr3 = ["Robin", "Morgan"];
const myChildren = arr1.concat(arr2, arr3);
```

```concat()``` 메서드는 문자열을 인수로 사용할 수도 있습니다.

###### 예제 14

```javascript
const arr1 = ["Emil", "Tobias", "Linus"];
const myChildren = arr1.concat("Peter"); 
```

## 스플라이싱 및 슬라이싱 배열

```splice()``` 메서드는 배열에 새 항목을 추가합니다.

```slice()``` 메서드는 배열의 일부를 잘라냅니다.

## 배열 splice()

```splice()``` 메서드는 배열에 새 항목을 추가하는 데 사용할 수 있습니다.

###### 예제 15

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 0, "Lemon", "Kiwi");
```

첫 번째 매개 변수(2)는 새 요소를 **추가**할 **위치**를 정의합니다(분할).

두 번째 매개 변수(0)는 **제거**할 **요소 수**를 정의합니다.

나머지 매개변수("Lemon", "Kiwi")는 **추가**할 새 요소를 정의합니다.

```splice()``` 메서드는 삭제된 항목이 있는 배열을 반환합니다.

###### 예제 16

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 2, "Lemon", "Kiwi");
```

## 배열 slice()

```slice()``` 메서드는 배열의 일부를 새 배열로 잘라냅니다.

이 예에서는 배열 요소 1("Orange")부터 시작하는 배열의 일부를 잘라냅니다.

###### 예제 17

```javascript
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(1);
```

{: .box-note}
```slice()``` 메서드는 새 배열을 만듭니다.<br>```slice()``` 메서드는 소스 배열에서 요소를 제거하지 않습니다.

이 예에서는 배열 요소 3("Apple")에서 시작하는 배열의 일부를 잘라냅니다.

###### 예제 18

```javascript
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(3);
```

```slice()``` 메서드는 ```slice(1, 3)```와 같은 두 개의 인수를 사용할 수 있습니다.

그런 다음 메소드는 시작 인수에서 요소를 선택하고 끝 인수까지는 포함하지 않습니다.

###### 예제 19

```javascript
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(1, 3);
```

첫 번째 예제와 같이 end 인수가 생략된 경우 ```slice()``` 메서드는 나머지 배열을 잘라냅니다.

###### 예제 20

```javascript
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(2);
```

## 자동 toString()

JavaScript는 원시 값이 필요할 때 배열을 쉼표로 구분된 문자열로 자동 변환합니다.

이것은 항상 배열을 출력하려고 할 때 해당됩니다.

이 두 가지 예에서는 동일한 결과가 나타납니다.

###### 예제 21

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.toString();
```

###### 예제 22

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits;
```

{: .box-note}
모든 JavaScript 개체에는 toString() 메서드가 있습니다.
