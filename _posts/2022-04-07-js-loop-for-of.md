---
layout: post
title: JavaScript 40. for of 반복문 (For Of Loop)
subtitle: 반복 가능한 객체를 반복하는 for of 반복에 대해 알아봅니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript for of 반복문

## for of 반복문

반복 가능한 객체의 값을 반복합니다.

이를 통해 배열, 문자열, 맵, 노드 리스트 등과 같은 반복 가능한 데이터 구조를 루프할 수 있습니다.

#### 구문

```javascript
for (variable of iterable) {
  // 실행할 코드 블록
}
```

**variable** - 매 반복마다 다음 속성의 값이 변수에 할당됩니다. 변수는 ```const```, ```let``` 또는 ```var```로 선언할 수 있습니다.

**iterable** - 반복 가능한 속성을 가진 객체입니다.

#### 지원 브라우저

**For/of** 2015년 자바스크립트에 추가됐습니다.(ES6)

| 브라우저 | 구글 Chrome | 마이크로소프트 Edge | Firefox | Safari | Opera |
| 버전 | 38 | 12 | 51 | 7 | 25 |

**for/of**는 Internet Explorer에서 지원되지 않습니다.

## 배열에서 반복

###### 예제 1

```javascript
const cars = ["BMW", "Volvo", "Mini"];

let text = "";
for (let x of cars) {
  text += x;
}
```

## 문자열에서 반복

###### 예제 2

```javascript
let language = "JavaScript";

let text = "";
for (let x of language) {
text += x;
}
```

