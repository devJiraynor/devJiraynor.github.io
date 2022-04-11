---
layout: post
title: JavaScript 46. 형 변환 (Type Conversion)
subtitle: JavaScript 형 변환에 대해 알아봅니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 형 변환

## 형 변환

자바스크립트 변수는 새로운 변수와 다른 데이터 유형으로 변환할 수 있습니다.

+ JavaScript 함수 사용
+ JavaScript 자체 **자동** 변환

## 문자열을 숫자로 변환

글로벌 메서드 ```Number()```는 문자열을 숫자로 변환할 수 있습니다.

숫자를 포함하는 문자열(예: "3.14")은 숫자로 변환된다.

빈 문자열은 0으로 변환됩니다.

다른 모든 항목은 ```NaN```으로 변환됩니다.

###### 예제 1

```javascript
Number("3.14")    // returns 3.14
Number(" ")       // returns 0
Number("")        // returns 0
Number("99 88")   // returns NaN
```

## 단항 + 연산자

**단항 + 연산자**를 사용하여 변수를 숫자로 변환할 수 있습니다.

###### 예제 2

```javascript
let y = "5";      // y : string
let x = + y;      // x : number
```

변수를 변환할 수 없는 경우에는 ```NaN```을 반환합니다.

###### 예제 3

```javascript
let y = "John";   // y : string
let x = + y;      // x : number (NaN)
```

## 숫자를 문자열로 변환

전역 메서드 ```String()```은 숫자를 문자열로 변환할 수 있습니다.

모든 유형의 숫자, 리터럴, 변수 또는 식에 사용할 수 있습니다.

###### 예제 4

```javascript
String(x)         
String(123)       
String(100 + 23)  
```

Number 메서드 ```toString()```도 같은 작업을 수행합니다.

###### 예제 5

```javascript
x.toString()
(123).toString()
(100 + 23).toString()
```

## 날짜를 숫자로 변환

글로벌 메서드 ```Number()```를 사용하여 날짜를 숫자로 변환할 수 있습니다.

###### 예제 6

```javascript
d = new Date();
Number(d)       
```

Date 메서드 ```getTime()```도 같은 작업을 수행합니다.

###### 예제 7

```javascript
d = new Date();
d.getTime()      
```

## 날짜를 문자열로 변환

전역 메서드 ```String()```은 날짜를 문자열로 변환할 수 있습니다.

###### 예제 8

```javascript
String(Date())
```

Date 메서드 ```toString()```도 같은 작업을 수행합니다.

###### 예제 9

```javascript
Date().toString()
```

## 부울을 숫자로 변환

글로벌 메서드 ```Number()```는 부울을 숫자로 변환할 수도 있습니다.

###### 예제 10

```javascript
Number(false)     // returns 0
Number(true)      // returns 1
```

## 부울을 문자열로 변환

전역 메서드 ```String()```은 부울을 문자열로 변환할 수 있습니다.

###### 예제 11

```javascript
String(false)      // returns "false"
String(true)       // returns "true"
```

Boolean 메서드 ```toString()```도 같은 작업을 수행합니다.

###### 예제 12

```javascript
false.toString()   // returns "false"
true.toString()    // returns "true"
```

## 자동 형 변환

JavaScript가 "잘못된" 데이터 유형에서 작동하려고 할 때, 값을 "올바른" 유형으로 변환하려고 할 것입니다.

결과는 항상 예상한 대로만 나타나는 것은 아닙니다.

###### 예제 13

```javascript
5 + null    // returns 5         
"5" + null  // returns "5null"   
"5" + 2     // returns "52"      
"5" - 2     // returns 3         
"5" * "2"   // returns 10        
```

## 자동 문자열 변환

자바스크립트는 객체나 변수를 "출력"하려고 할 때 변수의 ```toString()``` 함수를 자동으로 호출합니다.

###### 예제 14

```javascript
document.getElementById("demo").innerHTML = myVar;

// myVar = {name:"Fjohn"}  // "[object Object]"
// myVar = [1,2,3,4]       // "1,2,3,4"
// myVar = new Date()      // "Fri Jul 18 2014 09:08:55 GMT+0200"
```

숫자와 부울도 변환되지만, 이는 그다지 눈에 띄지 않습니다.

```javascript
// if myVar = 123             // "123"
// if myVar = true            // "true"
// if myVar = false           // "false"
```
