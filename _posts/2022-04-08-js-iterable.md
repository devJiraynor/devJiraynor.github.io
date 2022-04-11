---
layout: post
title: JavaScript 43. 반복 가능 객체 (Iterables)
subtitle: Iterables는 반복 가능한 객체입니다. Iterables는 간단하고 효율적인 코드로 접근할 수 있습니다. Iterables는 for..of 반복문으로 반복할 수 있습니다
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 반복가능 객체

## for of 반복문

```for..of``` 문은 반복 가능한 객체의 요소를 순환합니다.

#### 구문

```javascript
for (variable of iterable) {
  // 실행할 코드 블록
}
```

## Iterating

Iterating은 이해하기 쉽습니다.

단순히 일련의 요소들에 대한 루프를 의미합니다.

다음은 몇 가지 쉬운 예입니다.

+ 문자열에서 반복
+ 배열에서 반복

## 문자열에서 반복

```for..of``` 루프를 사용하여 문자열의 요소를 반복할 수 있습니다.

###### 예제 1

```javascript
const name = "W3Schools";

for (const x of name) {
  // 실행할 코드 블록
}
```

## 배열에서 반복

```for..of``` 루프를 사용하여 배열의 요소를 반복할 수 있습니다.

###### 예제 2

```javascript
const letters = ["a","b","c"];

for (const x of letters) {
  // 실행할 코드 블록
}
```
