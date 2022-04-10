---
layout: post
title: JavaScript 35. 비교 및 논리 연산자 (Comparison and Logical Operators)
subtitle: 비교 연산자와 논리 연산자는 참 또는 거짓을 검정하는 데 사용됩니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 비교 및 논리 연산자

## 비교 연산자

비교 연산자는 변수 또는 값 간의 동일성 또는 차이를 결정하기 위해 논리 구문에서 사용됩니다.

x = 5인 경우 아래 표에서는 비교 연산자를 설명합니다.

#### ```==``` - 같다

| **비교 식** | **결과** |
| ```x == 8``` | false |
| ```x == 5``` | true |
| ```x == "5"``` | true |

#### ```===``` - 값과 타입이 모두 같다

| **비교 식** | **결과** |
| ```x === 5``` | true |
| ```x === "5"``` | false |

#### ```!=``` - 다르다

| **비교 식** | **결과** |
| ```x == 8``` | true |

#### ```!==``` - 값 또는 타입이 다르다

| **비교 식** | **결과** |
| ```x !== 5``` | false |
| ```x !== "5"``` | true |
| ```x !== 8``` | true |

#### ```>``` - 크다

| **비교 식** | **결과** |
| ```x > 8``` | false |

#### ```<``` - 작다

| **비교 식** | **결과** |
| ```x < 8``` | true |

#### ```>=``` - 크거나 같다

| **비교 식** | **결과** |
| ```x >= 8``` | false |

#### ```<=``` - 작거나 같다

| **비교 식** | **결과** |
| ```x <= 8``` | true |

## 사용 방법

비교 연산자는 조건문에서 값을 비교하고 결과에 따라 조치를 취하기 위해 사용할 수 있습니다.

```javascript
if (age < 18) text = "Too young to buy alcohol";
```

## 논리 연산자

논리 연산자는 변수 또는 값 사이의 논리를 결정하는 데 사용됩니다.

아래 표는 **x = 6**과 **y = 3**이 주어졌을 때 논리 연산자를 설명합니다.

| **연산자** | **설명** | **예** |
| ```&&``` | and | (x < 10 && y > 1) : true |
| ```||``` | or | (x == 5 || y == 5) : false |
| ```!``` | not | !(x == y) : true |

## 조건(삼항) 연산자

자바스크립트에는 특정 조건에 따라 변수에 값을 할당하는 조건 연산자도 포함되어 있습니다.

#### 구문

```javascript
variablename = (condition) ? value1:value2 
```

###### 예제 1

```javascript
let voteable = (age < 18) ? "Too young":"Old enough";
```

변수 ```age```가 18세 미만인 경우 변수 ```voteable``` 값은 "Too young"이 되고, 그렇지 않은 경우 "Old enough"가 됩니다.

## 서로 다른 타입 비교

서로 다른 유형의 데이터를 비교하면 예기치 않은 결과가 발생할 수 있습니다.

문자열과 숫자를 비교할 때 JavaScript는 문자열을 숫자로 변환합니다. 빈 문자열은 0으로 변환됩니다. 숫자가 아닌 문자열은 항상 거짓인 NaN으로 변환됩니다.

| **비교식** | **결과** |
| ```2 < 12``` | true |
| ```2 < "12"``` | true |
| ```2 < "John"``` | false |
| ```2 > "John"``` | false |
| ```2 == "John"``` | fasle |
| ```"2" < "12"``` | false |
| ```"2" > "12"``` | true |
| ```"2" == "12"``` | fasle |

두 문자열을 비교할 때 "2"는 "12"보다 크며 이는 1은 2보다 사전상 빠르기 때문입니다.

적절한 결과를 얻으려면 비교하기 전에 변수를 적절한 유형으로 변환해야 합니다.

###### 예제 2

```javascript
age = Number(age);
if (isNaN(age)) {
  voteable = "Input is not a number";
} else {
  voteable = (age < 18) ? "Too young" : "Old enough";
}
```
