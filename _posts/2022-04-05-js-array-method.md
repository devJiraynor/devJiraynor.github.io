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

