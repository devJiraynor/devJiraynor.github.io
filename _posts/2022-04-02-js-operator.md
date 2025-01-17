---
layout: post
title: JavaScript 10. 연산자 (Operator)
subtitle: JavaScript의 연산자를 알아봅니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 연산자

<br>

###### 예제 1 - 변수에 값을 할당하고 함께 추가합니다.

```javascript
let x = 5;         // x에 5를 할당합니다.
let y = 2;         // y에 5를 할당합니다.
let z = x + y;     // z에 x + y(5 + 2)를 할당합니다.
```

**할당*** 연산자(```=```)는 변수에 값을 할당합니다.

###### 할당 연산자

```javascript
let x = 10;
```

**더하기** 연산자(```+```)는 숫자를 서로 더합니다.

###### 덧셈 연산자

```javascript
let x = 5;
let y = 2;
let z = x + y;
```

**곱셈** 연산자(```*```)는 숫자를 서로 곱합니다.

###### 곱셈 연산자

```javascript
let x = 5;
let y = 2;
let z = x * y;
```

## 산술 연산자

산술 연산자는 숫자에 대해 산술을 수행하는 데 사용됩니다.

| **연산자** | **설명** |
| ```+``` | 덧셈 연산자 |
| ```-``` | 뺄셈 연산자 |
| ```*``` | 곱셈 연산자 |
| ```**``` | 제곱 연산자 (ES6부터 제공) |
| ```/``` | 나누기 연산자 |
| ```%``` | 나머지 연산자 |
| ```++``` | 증가 연산자 |
| ```--``` | 감소 연산자 |

## 할당 연산자

할당 연산자는 JavaScript 변수에 값을 할당합니다.

| **연산자** | **예** | **같은 값** |
| ```=``` | ```x = y``` | ```x = y```|
| ```+=``` | ```x += y``` | ```x = x + y```|
| ```-=``` | ```x -= y``` | ```x = x - y```|
| ```*=``` | ```x *= y``` | ```x = x * y```|
| ```/=``` | ```x /= y``` | ```x = x / y```|
| ```%=``` | ```x %= y``` | ```x = x % y```|
| ```**=``` | ```x **= y``` | ```x = x ** y```|

**덧셈 할당** 연산자(```+=```)는 변수에 값을 추가합니다.

###### 덧셈 할당 연산자

```javascript
let x = 10;
x += 5;
```

## 문자열 연산자

```+``` 연산자를 사용하여 문자열을 연결할 수 있습니다.

###### 예제 2

```javascript
let text1 = "John";
let text2 = "Doe";
let text3 = text1 + " " + text2;
```

결과 : 

<samp>John Doe</samp>

```+=``` 할당 연산자를 사용하여 문자열을 연결할 수도 있습니다.

###### 예제 3

```javascript
let text1 = "What a very ";
text1 += "nice day";
```

결과 :

<samp>What a very nice day</samp>

{: .box-note}
문자열에서 ```+``` 연산자를 사용할 경우 연결 연산자라고 합니다.

## 문자열과 숫자 연결

두 개의 숫자를 더하면 합계가 반환되지만 숫자와 문자열을 추가하면 문자열이 반환됩니다.

###### 예제 4

```javascript
let x = 5 + 5;
let y = "5" + 5;
let z = "Hello" + 5;
```

결과 : 

<samp>10<br>55<br>Hello5</samp>
 
{: .box-note}
숫자와 문자열을 추가하면 문자열이 됩니다!

## 비교 연산자

| **연산자** | **설명** |
| ```==``` | 같음 |
| ```===``` | 값과 타입이 모두 같음 |
| ```!=``` | 다름 |
| ```!==``` | 값 또는 타입이 다름 |
| ```>``` | 큼 |
| ```<``` | 작음 |
| ```>=``` | 크거나 같음 |
| ```<=```| 작거나 같음 |
| ```?``` | 삼항 연산자 |

## 논리 연산자

| **연산자** | **설명** |
| ```&&``` | 논리 곱 |
| ```||``` | 논리 합 |
| ```!``` | 부정 |

## 타입 연산자

| **typeof** | **설명** |
| ```typeof``` | 변수 타입 반환 |
| ```instanceof``` | 객체가 객체 유형의 인스턴스인 경우 true를 반환 |

## 비트 연산자

비트 연산자는 32비트 숫자로 동작합니다.

조작의 모든 숫자 오퍼랜드는 32비트 숫자로 변환됩니다. 결과는 JavaScript 번호로 변환됩니다.

| **연산자** | **설명** | **예** | **같은 값** | **결과** | **10진수** |
| ```&``` | AND | ```5 & 1``` | ```0101 & 0001``` | 0001 | 1 |
| ```|``` | OR | ```5 | 1``` | ```0101 | 0001``` | 0101 | 5 |
| ```~``` | NOT | ```~ 5``` | ``` ~0101``` | 1010 | 10 |
| ```^``` | XOR | ```5 ^ 1``` | ```0101 ^ 0001``` | 0100 | 4 |
| ```<<``` | left shift | ```5 << 1``` | ```0101 << 1``` | 1010 | 10 |
| ```>>``` | right shift | ```5 >> 1``` | ```0101 >> 1``` | 0010 | 2 |
| ```>>>``` | unsigned right shift | ```5 >>> 1``` | ```0101 >>> 1``` | 0010 | 2 |

{: .box-note}
위의 예에서는 4비트 부호 없는 예를 사용합니다. 그러나 JavaScript는 32비트 서명된 숫자를 사용합니다. <br>따라서 JavaScript에서는 최대 5는 10을 반환하지 않습니다. -6이 반환됩니다.<br>~0000000000000000000000000000000000101은 1111111111111111111111111110을 반환합니다.
