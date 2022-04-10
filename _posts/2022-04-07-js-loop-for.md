---
layout: post
title: JavaScript 38. for 반복문 (For Loop)
subtitle: 반복문은 코드 블록을 여러 번 실행할 수 있습니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript for 반복문

## 반복문(Loop)

반복문은 매번 다른 값을 사용하여 동일한 코드를 반복해서 실행하려는 경우에 유용합니다.

배열을 사용하는 경우 다음과 같은 경우가 많습니다.

###### 예제 1

```javascript
text += cars[0] + "<br>";
text += cars[1] + "<br>";
text += cars[2] + "<br>";
text += cars[3] + "<br>";
text += cars[4] + "<br>";
text += cars[5] + "<br>";
```

위의 문장 대신에 아래와 같이 쓸수 있습니다.

###### 예제 2

```javascript
for (let i = 0; i < cars.length; i++) {
  text += cars[i] + "<br>";
}
```

## 여러 종류의 반복문

자바스크립트는 다양한 종류의 반복문을 지원합니다.

+ ```for``` - 코드 블록을 여러 번 반복합니다.
+ ```for/in``` - 객체의 속성을 반복합니다.
+ ```for/of``` - 반복 가능한 객체의 값을 반복합니다.
+ ```while``` - 지정된 조건이 참일 때 코드 블록을 반복합니다.
+ ```do/while``` - 지정된 조건이 참일 때 코드 블록을 루프합니다. (무조건 한번은 실행)

## for 반복문

```for``` 반복의 구문은 다음과 같습니다.

```javascript
for (statement 1; statement 2; statement 3) {
  // 실행할 코드 블록
}
```

**statement 1**은 코드 블록의 실행 전에 한 번 실행됩니다.

**statement 2**는 코드 블록을 실행하기 위한 조건을 정의합니다.

**statement 3**은 코드 블록이 실행된 후 매번 실행됩니다.

###### 예제 1

```javascript
for (let i = 0; i < 5; i++) {
  text += "The number is " + i + "<br>";
}
```

위의 예에서 다음을 읽을 수 있습니다.

statement 1은 루프가 시작되기 전에 변수를 초기화합니다(예: let i = 0).

statement 2는 루프가 실행될 조건을 정의합니다(i는 5보다 작아야 함).

statement 3은 루프의 코드 블록이 실행될 때마다 값(i++)을 증가시킵니다.

## Statement 1

일반적으로 Statement 1을 사용하여 루프에 사용되는 변수를 초기화합니다(예: let i = 0).

필수 사항은 아니며, 선택 사항입니다.

Statement 1(쉼표로 구분)에서 많은 값을 초기화할 수 있습니다.

###### 예제 2

```javascript
for (let i = 0, len = cars.length, text = ""; i < len; i++) {
  text += cars[i] + "<br>";
}
```

Statement 1을 생략할 수 있습니다(루프가 시작되기 전에 값이 설정되는 경우 등).

###### 예제 3

```javascript
let i = 2;
let len = cars.length;
let text = "";
for (; i < len; i++) {
  text += cars[i] + "<br>";
}
```

## Statement 2

Statement 2는 종종 초기 변수의 조건을 평가하는 데 사용됩니다.

필수 사항은 아니며, 선택 사항입니다.

Statement 2가 true를 반환하면 루프가 다시 시작되고, false를 반환하면 루프가 종료됩니다.

{: .box-note}
Statement 2를 생략할 경우 루프 내부에 ```break```를 사용해야 합니다. 그렇지 않으면 루프가 절대 끝나지 않고 브라우저가 중단됩니다.

## Statement 3

Statement 3은 초기 변수의 값을 증가시킵니다.

필수 사항은 아니며, 선택 사항입니다.

Statement 3은 음의 증가(i-), 양의 증가(i = i + 15) 또는 다른 모든 것을 할 수 있습니다.

Statement 3은 루프 내부에서 값을 증가시키는 경우 생략할 수도 있습니다.

###### 예제 4

```javascript
let i = 0;
let len = cars.length;
let text = "";
for (; i < len; ) {
  text += cars[i] + "<br>";
  i++;
}
```

## 반복문 범위

반복문에서 ```var``` 사용

###### 예제 5

```javascript
var i = 5;

for (var i = 0; i < 10; i++) {
  // 실행 코드
}

// i : 10
```

반복문에서 ```let``` 사용

###### 예제 6

```javascript
let i = 5;

for (let i = 0; i < 10; i++) {
  // 실행 코드
}

// i : 5
```

첫 번째 예에서는 ```var```를 사용하여 반복문에서 선언된 변수가 반복문 외부에 있는 변수를 다시 선언합니다.

두 번째 예에서는 ```let```을 사용하여 반복문에서 선언된 변수는 반복문 외부에 있는 변수를 다시 선언하지 않습니다.

```let```을 사용하여 루프에서 ```i``` 변수를 선언하면, ```i``` 변수는 루프 내에서만 사용할 수 있습니다.

