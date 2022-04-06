---
layout: post
title: JavaScript 18. 문자열 메서드 (String Method)
subtitle: 문자열 메서드는 문자열을 사용하는 데 도움이 됩니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 문자열 메서드

## 문자열 메서드 및 속성

"John Doe"와 같은 원시 값은 객체가 아니기 때문에 속성이나 메서드를 가질 수 없습니다.

그러나 자바스크립트는 메소드와 속성을 실행할 때 원시 값을 객체로 취급하기 때문에 자바스크립트에서는 원시 값도 사용할 수 있습니다.

## 문자열 길이

```length``` 속성은 문자열의 길이를 반환합니다.

###### 예제 1

```javascript
let txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
let length = txt.length;
```

## 문자열 요소 추출

문자열의 일부를 추출하는 방법에는 세 가지가 있습니다.

+ ```slice(start, end)```
+ ```substring(start, end)```
+ ```substr(start, length)```

## slice()

```slice()```는 문자열의 일부를 추출하고 추출된 부분을 새 문자열로 반환합니다.

이 메서드는 시작 위치와 끝 위치(끝은 포함되지 않음)의 두 가지 매개 변수를 사용합니다.

이 예에서는 문자열의 일부를 위치 7에서 위치 12(13-1)까지 슬라이스합니다.

###### 예제 2

```javascript
let str = "Apple, Banana, Kiwi";
let part = str.slice(7, 13);
```

{: .box-note}
JavaScript는 0부터 위치를 계산합니다.<br>첫 번째 위치는 0입니다.<br>두 번째 위치는 1입니다.

파라미터가 음수이면 문자열 끝에서 위치가 카운트됩니다.

이 예에서는 문자열의 일부를 위치 -12에서 위치 -6까지 슬라이스합니다.

###### 예제 3

```javascript
let str = "Apple, Banana, Kiwi";
let part = str.slice(-12, -6);
```

두 번째 매개 변수를 생략하면 문자열 끝까지 잘립니다.

###### 예제 4

```javascript
let part = str.slice(7);
```

이 경우 음수를 사용하여 끝에서 부터 셀수도 있습니다.

###### 예제 5

```javascript
let part = str.slice(-12);
```

## substring()

```substring()```은 ```slice()```와 유사합니다.

차이점은 ```substring()```은 음의 인덱스를 사용할 수 없다는 것입니다.

###### 예제 6

```javascript
let str = "Apple, Banana, Kiwi";
let part = str.substring(7, 13);
```

두 번째 매개 변수를 생략하면 ```substring()```이 문자열 끝까지 잘라냅니다.

## substr()

```substr()```은 ```slice()```와 유사합니다.

차이점은 두 번째 매개 변수가 추출될 문자의 **길이**를 지정한다는 것입니다.

###### 예제 7

```javascript
let str = "Apple, Banana, Kiwi";
let part = str.substr(7, 6);
```

두 번째 매개 변수를 생략하면 ```substr()```이 문자열 끝까지 잘라냅니다.

###### 예제 8

```javascript
let str = "Apple, Banana, Kiwi";
let part = str.substr(7);
```

첫 번째 파라미터가 음수일 경우 문자열의 끝에서 위치가 카운트됩니다.

###### 예제 9

```javascript
let str = "Apple, Banana, Kiwi";
let part = str.substr(-4);
```

## 문자열 내용 변경

```replace()``` 메서드는 지정된 값을 문자열의 다른 값으로 바꿉니다.

###### 예제 10

```javascript
let text = "Please visit Microsoft!";
let newText = text.replace("Microsoft", "Windows");
```

{: .box-note}
```replace()``` 메서드는 호출된 문자열을 변경하지 않습니다.<br>```replace()``` 메서드는 새 문자열을 반환합니다.<br>```replace()``` 메서드는 첫 번째 일치 항목만 바꿉니다.<br>모든 일치 항목을 바꾸려면 /g 플래그 집합과 함께 정규식을 사용하십시오.

기본적으로 ```replace()``` 메서드는 **첫 번째 일치 항목**만 대체합니다.

###### 예제 11

```javascript
let text = "Please visit Microsoft and Microsoft!";
let newText = text.replace("Microsoft", "Windows");
```

기본적으로 ```replace()``` 메서드는 대소문자를 구분합니다. MICROSOFT는 사용할 수 없습니다.

###### 예제 12

```javascript
let text = "Please visit Microsoft!";
let newText = text.replace("MICROSOFT", "Windows");
```

대/소문자를 구분하지 않으려면 정규식을 ```/i``` 플래그(구체적이지 않음)와 함께 사용합니다.

###### 예제 13

```javscript
let text = "Please visit Microsoft!";
let newText = text.replace(/MICROSOFT/i, "Windows");
```

{: .box-note}
정규식은 따옴표 없이 작성됩니다.

모든 일치 항목을 바꾸려면 정규식을 /g 플래그(글로벌 일치)와 함께 사용합니다.

###### 예제 14

```javascript
let text = "Please visit Microsoft and Microsoft!";
let newText = text.replace(/Microsoft/g, "Windows");
```

## 대/소문자로 변환

```toUpperCase()```을 사용하면 문자열이 대문자로 변환됩니다.

```toLowerCase()```을 사용하면 문자열이 소문자로 변환됩니다.

## toUpperCase()

###### 예제 15

```javascript
let text1 = "Hello World!";
let text2 = text1.toUpperCase();
```

## toLowerCase()

###### 예제 16

```javascript
let text1 = "Hello World!";      
let text2 = text1.toLowerCase();
```

## concat()

```concat()```은 두 개 이상의 문자열을 결합합니다.

###### 예제 17

```javascript
let text1 = "Hello";
let text2 = "World";
let text3 = text1.concat(" ", text2);
```

더하기 연산자 대신 ```concat()``` 메서드를 사용할 수 있습니다. 아래 두 구문은 같은 역할을 합니다.

###### 예제 18

```javascript
text = "Hello" + " " + "World!";
text = "Hello".concat(" ", "World!");
```

{: .box-note}
모든 문자열 메서드는 새 문자열을 반환합니다. 원래 문자열은 수정하지 않습니다.

## trim()

```trim()``` 메서드는 문자열의 양쪽에서 공백을 제거합니다.

###### 예제 19

```javascript
let text1 = "      Hello World!      ";
let text2 = text1.trim();
```

## 문자열 패딩

ECMAScript 2017은 문자열의 시작과 끝에 패딩을 지원하기 위해 ```padStart()```와 ```padEnd()```라는 두 가지 문자열 메서드를 추가했습니다.

## padStart()

```padStart()``` 메서드는 문자열을 다른 문자열로 패딩합니다.

###### 예제 20

```javascript
let text = "5";
let padded = text.padStart(4,"x");
```

###### 예제 21

```javascript
let text = "5";
let padded = text.padStart(4,"0");
```

{: .box-note}
```padStart()``` 메서드는 문자열 메서드입니다.<br>숫자를 패딩하려면 먼저 숫자를 문자열로 변환합니다.

###### 예제 22

```javascript
let numb = 5;
let text = numb.toString();
let padded = text.padStart(4,"0");
```

## padStart() 지원 브라우저

```padStart()```는 ECMA스크립트 2017의 기능입니다.

모든 최신 브라우저에서 지원됩니다.

```padStart()```는 Internet Explorer에서 지원되지 않습니다.

## padEnd()

```padEnd()``` 메서드는 문자열을 다른 문자열로 패딩합니다.

###### 예제 23

```javascript
let text = "5";
let padded = text.padEnd(4,"x");
```

###### 예제 24

```javascript
let text = "5";
let padded = text.padEnd(4,"0");
```

{: .box-note}
```padEnd()``` 메서드는 문자열 메서드입니다.<br>숫자를 패딩하려면 먼저 숫자를 문자열로 변환합니다.

###### 예제 25

```javascript
let numb = 5;
let text = numb.toString();
let padded = text.padEnd(4,"0");
```

## padEnd() 지원 브라우저

```padEnd()```는 ECMA스크립트 2017의 기능입니다.

모든 최신 브라우저에서 지원됩니다.

```padEnd()```는 Internet Explorer에서 지원되지 않습니다.

## 문자열 문자 추출

문자열 문자를 추출하는 방법에는 세 가지가 있습니다.

+ ```charAt(position)```
+ ```charCodeAt(position)```
+ 속성 접근 ```[]```

## charAt()

```charAt()``` 메서드는 문자열의 지정된 인덱스(위치)에 있는 문자를 반환합니다.

###### 예제 26

```javascript
let text = "HELLO WORLD";
let char = text.charAt(0);
```

## charCodeAt()

```charCodeAt()``` 메서드는 문자열의 지정된 인덱스에 있는 문자의 유니코드를 반환합니다.

메서드는 UTF-16 코드(0과 65535 사이의 정수)를 반환합니다.

###### 예제 27

```javascript
let text = "HELLO WORLD";
let char = text.charCodeAt(0);
```

## 속성 접근

ECMAScript 5(2009)는 문자열에서 속성 접근 ```[]```를 허용합니다.

###### 예제 28

```javascript
let text = "HELLO WORLD";
let char = text[0];
```

속성 액세스는 **예측할 수 없습니다.**

+ 문자열이 배열처럼 보이지만 실제로는 그렇지 않습니다.
+ 문자가 없으면 [ ]은 정의되지 않은 문자열을 반환하고 ```charAt()```는 빈 문자열을 반환합니다.
+ 읽기 전용입니다. ```str[0] = "A"```는 오류가 발생하지 않습니다.(하지만 작동하지 않습니다!)

###### 예제 29

```javascript
let text = "HELLO WORLD";
text[0] = "A";    // 오류가 발생하지 않지만, 작동하지도 않습니다.
```

## 문자열을 배열로 변환

{: .box-note}
문자열을 배열로 작업하기위해 문자열을 배열로 변환할 수 있습니다.

## split()

문자열은 ```split()``` 메서드를 사용하여 배열로 변환할 수 있습니다.

###### 예제 30

```javascript
text.split(",")    // , 로 나누기
text.split(" ")    // 공백으로 나누기
text.split("|")    // | 로 나누기
```

구분 기호를 생략하면 반환된 배열에 인덱스 ```[0]```의 전체 문자열이 포함됩니다.

구분 기호가 ""인 경우 반환되는 배열은 단일 문자의 배열이 됩니다.

###### 예제 31

```javascript
text.split("")
```
