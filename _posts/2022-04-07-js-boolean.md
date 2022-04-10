---
layout: post
title: JavaScript 34. 불리언 (Booleans)
subtitle: JavaScript Boolean은 true와 false의 두 가지 값 중 하나를 나타냅니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 불리언

## 불리언 값

프로그래밍에서는 다음과 같은 두 가지 값 중 하나만 가질 수 있는 데이터 유형이 필요할 수 있습니다.

+ YES / NO
+ ON / OFF
+ TRUE / FALSE

이를 위해 JavaScript에는 **boolean** 데이터 유형이 있습니다. 값은 **true** 또는 **false**만 사용할 수 있습니다.

## Boolean() 함수

```Boolean()``` 함수를 사용하여 식(또는 변수)이 참인지 확인할 수 있습니다.

###### 예제 1

```javascript
Boolean(10 > 9)
```

더 쉬운 방법:

```javascript
(10 > 9)
10 > 9
```

## 비교 연산자와 조건문

식의 부울 값은 모든 JavaScript 비교 및 조건의 기준이 됩니다.

| **연산자** | **설명** | **예** |
| ```==``` | 같다 | ```if (day == "Monday")``` |
| ```>``` | 크다 | ```if (salary > 9000)``` |
| ```<``` | 작다 | ```if (age < 18)``` |

## "값"이 있는 모든 것은 참

###### 예제 2

```javascript
100

3.14

-15

"Hello"

"false"

7 + 1 + 3.14
```

## "값"이 없는 모든 것은 거짓

0은 false입니다.

###### 예제 3

```javascript
let x = 0;
Boolean(x);
```

-0은 false입니다.

###### 예제 4

```javascript
let x = -0;
Boolean(x);
```

""(빈 문자열)은 false입니다.

###### 예제 5

```javscript
let x = "";
Boolean(x);
```

undefined는 false입니다.

###### 예제 6

```javascript
let x;
Boolean(x);
```

null은 false입니다.

###### 예제 7

```javascript
let x = null;
Boolean(x);
```

boolean 값 false는 false입니다.

###### 예제 8

```javascript
let x = false;
Boolean(x);
```

NaN은 false입니다.

###### 예제 9

```javascript
let x = 10 / "Hallo";
Boolean(x);
```

## 객체로써 Boolean

일반적으로 자바스크립트 부울은 리터럴에서 생성된 원시 값입니다.

```javascript
let x = false;
```

그러나 부울은 다음과 같은 ```new``` 키워드를 가진 객체로 정의될 수도 있습니다.

```javascript
let y = new Boolean(false);
```

###### 예제 10

```javascript
let x = false;
let y = new Boolean(false);

// typeof x returns boolean
// typeof y returns object
```

{: .box-note}
부울 객체를 만들지 마십시오.<br>```new``` 키워드는 코드를 복잡하게 만들고 실행 속도를 느리게 합니다.<br>부울 객체는 예기치 않은 결과를 초래할 수 있습니다.

###### 예제 11 - ```==``` 연산자를 사용할 때 x와 y는 같습니다.

```javascript
let x = false;
let y = new Boolean(false);

x == y
```

###### 예제 12 - ```===``` 연산자를 사용할 때 x와 y는 같지 않습니다.

```javascript
let x = false;
let y = new Boolean(false);

x === y
```

{: .box-note}
(x==y)와 (x===y)의 차이를 확인합니다.

###### 예제 13 - (x == y)는 참? 거짓?

```javascript
let x = new Boolean(false);
let y = new Boolean(false);
```

###### 예제 14 - (x === y)는 참? 거짓?

```javascript
let x = new Boolean(false);
let y = new Boolean(false);
```

{: .box-note}
두 JavaScript 개체를 비교하면 **항상** **false**가 반환됩니다.

