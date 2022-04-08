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

## Number() 메서드

Number()는 자바스크립트 변수를 숫자로 변환하는 데 사용할 수 있다.

###### 예제 6

```javascript
Number(true);
Number(false);
Number("10");
Number("  10");
Number("10  ");
Number(" 10  ");
Number("10.33");
Number("10,33");
Number("10 33");
Number("John");
```

{: .box-note}
숫자를 변환할 수 없는 경우 ```NaN```이 반환됩니다.

## Date에서 Number() 메소드 사용

```Number()```는 날짜를 숫자로 변환할 수도 있습니다.

###### 예제 7

```javascript
Number(new Date("1970-01-01"))
```

{: .box-note}
Number() 메서드는 1970-01-01 이후 밀리초 수를 반환합니다.

1970-01-02와 1970-01-01 사이의 밀리초 수는 86400000입니다.

###### 예제 8

```javascript
Number(new Date("1970-01-02"))
```

###### 예제 9

```javascript
Number(new Date("2017-09-30"))
```

## parseInt() 메서드

parseInt()는 문자열을 구문 분석하고 정수를 반환합니다. 공백이 허용됩니다. 첫 번째 숫자만 반환됩니다.

###### 예제 10

```javascript
parseInt("-10");
parseInt("-10.33");
parseInt("10");
parseInt("10.33");
parseInt("10 20 30");
parseInt("10 years");
parseInt("years 10");
```

숫자를 변환할 수 없는 경우 ```NaN```이 반환됩니다.

## parseFloat() 메서드

```parseFloat()```은 문자열을 구문 분석하고 숫자를 반환합니다. 공백이 허용됩니다. 첫 번째 숫자만 반환됩니다.

###### 예제 11

```javascript
parseFloat("10");
parseFloat("10.33");
parseFloat("10 20 30");
parseFloat("10 years");
parseFloat("years 10");
```

숫자를 변환할 수 없는 경우 ```NaN```이 반환됩니다.

## 숫자 속성

| **속성** | **설명** |
| MAX_VALUE | JavaScript에서 가능한 최대 수를 반환합니다. |
| MIN_VALUE | JavaScript에서 가능한 최소 수를 반환합니다. |
| POSITIVE_INFINITY | 무한대를 나타냅니다(오버플로우 시 반환됨). |
| NEGATIVE_INFINITY | 음의 무한대를 나타냅니다(오버플로우 시 반환됨). |
| NaN | "숫자가 아님" 값을 나타냅니다. |

## MIN_VALUE 와 MAX_VALUE

```MAX_VALUE```는 JavaScript에서 가능한 최대 수를 반환합니다.

###### 예제 12

```javascript
let x = Number.MAX_VALUE;
```

```MIN_VALUE```는 JavaScript에서 가능한 가장 낮은 숫자를 반환합니다.

###### 예제 13

```javascript
let x = Number.MIN_VALUE;
```

## POSITIVE_INFINITY

###### 예제 14

```javascript
let x = Number.POSITIVE_INFINITY;
```

```POSITIC_INFINITY```는 오버플로 시 반환됩니다.

###### 예제 15

```javascript
let x = 1 / 0;
```

## NEGATIVE_INFINITY

###### 예제 16

```javascript
let x = Number.NEGATIVE_INFINITY;
```

```NEGATION_INFINITY```는 오버플로 시 반환됩니다.

###### 예제 17

```javascript
let x = -1 / 0;
```

## NaN - Not a Number

###### 예제 18

```javascript
let x = Number.NaN;
```

```NaN```은 숫자가 숫자가 아님을 나타내는 자바스크립트 예약 단어이다.

숫자가 아닌 문자열로 산술을 시도하면 ```NaN```이 됩니다.

###### 예제 19

```javascript
let x = 100 / "Apple";
```

## 변수에는 숫자 속성을 사용할 수 없습니다.

Number 속성은 Number라는 자바스크립트의 Number 객체 래퍼에 속합니다.

이러한 속성은 ```Number.MAX_VALUE```로만 액세스할 수 있습니다.

```myNumber.MAX_VALUE``` 변수, 식 또는 값인 ```undefined```를 사용하면 정의되지 않은 값이 반환됩니다.

###### 예제 20

```javascript
let x = 6;
x.MAX_VALUE
```
