---
layout: post
title: JavaScript 41. while 반복문 (While Loop)
subtitle: while 반복문은 지정된 조건이 참인 한 코드 블록을 실행할 수 있습니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript while 반복문

## while 반복문

```while``` 반복문은 지정된 조건이 참인 한 코드 블록을 반복합니다.

#### 구문

```javascript
while (condition) {
  // 실행할 코드 블록
}
```

다음 예제에서는 변수 i가 10보다 작으면 반복문 코드는 계속해서 실행됩니다.

###### 예제 1

```javascript
while (i < 10) {
  text += "The number is " + i;
  i++;
}
```

{: .box-note}
조건에 사용되는 변수를 증가시키는 것을 잊으면 루프가 절대 끝나지 않습니다. 브라우저가 중단됩니다.

## do while 반복문

```do while``` 반복문은 ```while``` 반복문의 변형입니다. 이 반복문은 조건이 참인지 확인하기 전에 코드 블록을 한 번 실행한 다음 조건이 참인 한 반복합니다.

#### 구문

```javascript
do {
  // 실행할 코드 블록
}
while (condition);
```

아래 예제에서는 ```do while``` 루프를 사용합니다. 조건이 false일지라도 루프는 항상 한 번 실행되는데, 이는 조건이 테스트되기 전에 코드 블록이 실행되기 때문이다.

###### 예제 2

```javascript
do {
  text += "The number is " + i;
  i++;
}
while (i < 10);
```

## for 와 while 비교

```for``` 반복문에 대해 Statement 1과 Statement 3이 생략된 상태에서 ```while``` 반복문이 ```for``` 반복문과 거의 같다는 것을 알게 될 것입니다.

이 예에서 반복은 ```for``` 반복문을 사용하여 cars 배열에서 차량 이름을 수집합니다.

###### 예제 3

```javascript
const cars = ["BMW", "Volvo", "Saab", "Ford"];
let i = 0;
let text = "";

for (;cars[i];) {
  text += cars[i];
  i++;
}
```

이 예에서 반복은 ```while``` 반복문을 사용하여 cars 배열에서 차량 이름을 수집합니다.

###### 예제 4

```javascript
const cars = ["BMW", "Volvo", "Saab", "Ford"];
let i = 0;
let text = "";

while (cars[i]) {
  text += cars[i];
  i++;
}
```
