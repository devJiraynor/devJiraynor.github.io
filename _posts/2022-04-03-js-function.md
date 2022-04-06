---
layout: post
title: JavaScript 14. 함수 (Function)
subtitle: JavaScript 함수는 특정 작업을 수행하도록 설계된 코드 블록입니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 함수

JavaScript 함수는 특정 작업을 수행하도록 설계된 코드 블록입니다.

JavaScript 함수는 "어떤것이" 호출할 때 실행됩니다.

## 함수 구문

JavaScript 함수는 ```function``` 키워드 뒤에 **함수 이름**, 괄호**()**를 사용하여 정의됩니다.

함수 이름에는 문자, 숫자, 밑줄 및 달러 기호를 포함할 수 있습니다(변수와 동일한 규칙).

괄호에는 쉼표로 구분된 파라미터 이름을 포함할 수 있습니다.
**(parameter1, parameter2, ...)**

함수에서 실행할 코드가 대괄호 {} 안에 있습니다.

```javascript
function name(parameter1, parameter2, parameter3) {
  // 실행 코드
}
```

함수 **파라미터**는 함수 정의의 괄호() 안에 나열됩니다.

함수 **인수**는 함수를 호출할 때 함수가 수신하는 **값**입니다.

함수 내에서 인수(파라미터)는 로컬 변수로 작동합니다.

{: .box-note}
함수는 다른 프로그래밍 언어에서 프로시저 또는 서브루틴과 거의 동일합니다.

## 함수 호출

함수 내부의 코드는 "어떤것이" **호출**할 때 실행됩니다.

+ 이벤트 발생 시
+ JavaScript 코드에서 호출되는 경우
+ 자체 호출(자동)

## 함수 Return

JavaScript가 ```return``` 에 도달하면 함수는 실행을 중지합니다.

함수가 문장에서 호출된 경우, 자바스크립트는 호출 문장 뒤에 코드를 실행하기 위해 "복귀" 합니다.

함수는 종종 **반환 값**을 계산합니다. 반환 값은 "호출문"에 "반환"됩니다.

###### 예제 1

```javascript
let x = myFunction(4, 3);   // 함수를 호출하면 반환 값은 x에 들어갑니다.

function myFunction(a, b) {
  return a * b;             // 함수는 a와 b의 곱을 반환합니다.
}
```

## 함수를 사용하는 이유

코드를 재사용할 수 있습니다. 코드를 한 번 정의하고 여러 번 사용합니다.

다른 인수에 동일한 코드를 여러 번 사용하여 다른 결과를 생성할 수 있습니다.

###### 예제 2

```javascript
function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
}
document.getElementById("demo").innerHTML = toCelsius(77);
```

## () 연산자가 함수를 호출

위의 예에서 Celsius는 함수 객체를 의미하며, Celsius()는 함수 결과를 의미합니다.

() 없이 함수에 액세스하면 함수 결과 대신 함수 객체가 반환됩니다.

###### 예제 3

```javascript
function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
}
document.getElementById("demo").innerHTML = toCelsius;
```

## 변수 값으로 사용되는 함수

함수를 모든 유형의 공식, 할당 및 계산에서 변수를 사용하는 것과 동일한 방법으로 사용할 수 있습니다.

###### 예제 4

```javascript
let x = toCelsius(77);
let text = "The temperature is " + x + " Celsius";
```

```javascript
let text = "The temperature is " + toCelsius(77) + " Celsius";
```

## 지역(Local) 변수

JavaScript 함수 내에서 선언된 변수는 함수의 **지역변수**가 됩니다.

지역 변수는 함수 내에서만 액세스할 수 있습니다.

###### 예제 5

```javascript
// 여기서는 carName 변수를 사용할 수 없습니다.

function myFunction() {
  let carName = "Volvo";
  // 여기서는 carName 변수를 사용할 수 있습니다.
}

// 여기서는 carName 변수를 사용할 수 없습니다.
```

로컬 변수는 함수 내부에서만 인식되므로 동일한 이름을 가진 변수는 다른 함수에서 사용할 수 있습니다.

로컬 변수는 함수가 시작되면 생성되고, 함수가 완료되면 삭제됩니다.
