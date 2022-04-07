---
layout: post
title: JavaScript 22. 숫자 메서드 (Number Method)
subtitle: 숫자 메서드는 숫자 작업을 수행하는 데 도움이 됩니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 숫자 메서드

## 숫자 메서드와 속성

3.14 또는 2014와 같은 원시 값은 객체가 아니기 때문에 속성 및 메서드를 가질 수 없습니다.

그러나 자바스크립트는 메소드와 속성을 실행할 때 원시 값을 객체로 취급하기 때문에 자바스크립트에서는 원시 값도 사용할 수 있습니다.

## toString() 메서드

```toString()``` 메서드는 숫자를 문자열로 반환합니다.
모든 숫자 방법은 모든 종류의 숫자(문자, 변수 또는 표현식)에 사용할 수 있다.

###### 예제 1

```javascript
let x = 123;
x.toString();
(123).toString();
(100 + 23).toString();
```

## toExponential() 메서드

```toExponential()```는 숫자 반올림 및 지수 표기법을 사용하여 쓴 문자열을 반환합니다.

매개 변수는 소수점 뒤의 문자 수를 정의합니다.

###### 예제 2

```javascript
let x = 9.656;
x.toExponential(2);
x.toExponential(4);
x.toExponential(6);
```

매개 변수는 선택 사항입니다. 지정하지 않으면 JavaScript가 반올림하지 않습니다.

## toFixed() 메서드

```toFixed()```는 지정된 소수점 수로 쓰여진 숫자와 함께 문자열을 반환합니다.

###### 예제 3

```javascript
let x = 9.656;
x.toFixed(0);
x.toFixed(2);
x.toFixed(4);
x.toFixed(6);
```

{: .box-note}
```toFixed(2)``` 화폐에 적용하기 적합합니다.

## toPrecision() 메서드

```toPrecision()```은 지정된 길이로 쓰여진 숫자의 문자열을 반환합니다.

###### 예제 4

```javascript
let x = 9.656;
x.toPrecision();
x.toPrecision(2);
x.toPrecision(4);
x.toPrecision(6);
```

## valueOf() 메서드

```valueOf()```는 숫자를 숫자로 반환합니다.

###### 예제 5

```javascript
let x = 123;
x.valueOf();
(123).valueOf();
(100 + 23).valueOf();
```

자바스크립트에서 숫자는 원시 값(= 번호 유형)이거나 객체(= 개체 유형)일 수 있습니다.

```valueOf()``` 메서드는 내부적으로 자바스크립트에서 Number 객체를 원시 값으로 변환하는 데 사용됩니다.

당신의 코드에 그것을 사용할 이유가 없습니다.

{: .box-note}
모든 JavaScript 데이터 유형에는 ```valueOf()```와 ```toString()``` 메서드가 있습니다.

## 변수를 숫자로 변환

변수를 숫자로 변환하는 데 사용할 수 있는 3가지 자바스크립트 메서드가 있습니다.

+ ```Number()``` 메서드
+ ```parseInt()``` 메서드
+ ```parseFloat()``` 메서드

이러한 메서드는 **숫자** 메서드가 아니라 **전역** JavaScript 메서드입니다.

## 전역 JavaScript 메서드

자바스크립트 전역 메서드는 모든 자바스크립트 데이터 형식에 사용할 수 있습니다.

숫자로 작업할 때 가장 적절한 방법은 다음과 같습니다.

| **메서드** | **설명** |
| ```Number()``` | 인수에서 변환된 숫자를 반환합니다. |
| ```parseFloat()``` | 인수를 구문 분석하고 부동 소수점 번호를 반환합니다. |
| ```parseInt()``` | 인수를 구문 분석하고 정수를 반환합니다. |

