---
layout: post
title: JavaScript 04. 문장 (Statement)
subtitle: Javascript 문법에 대해 알아봅니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 문장

## JavaScript 프로그램

**컴퓨터 프로그램**은 컴퓨터에 의해 "실행"되는 "명령"의 목록입니다.

프로그래밍 언어에서 이러한 프로그래밍 명령을 문이라고 합니다.

```JavaScript 프로그램```은 프로그래밍 ```문장```의 목록입니다.

## JavaScript 문장

JavaScript 문장은 값, 연산자, 식, 키워드 및 주석으로 구성됩니다.

이 문장은 브라우저에 "Hello Dolly."를 id="http"로 HTML 요소 안에 쓰라고 지시합니다.

###### 예제 1

```javascript
document.getElementById("demo").innerHTML = "Hello Dolly.";
```

대부분의 JavaScript 프로그램에는 많은 JavaScript 문장이 포함되어 있습니다.

{: .box-note}
문장은 작성된 순서대로 하나씩 실행됩니다.

## 세미콜론 ;

세미콜론은 JavaScript 문장을 구분합니다.

각 실행 파일의 마지막에 세미콜론을 추가합니다.

###### 예제 2

```javascript
let a, b, c;  // 3가지 변수 선언
a = 5;        // a에 5 할당
b = 6;        // b에 6 할당
c = a + b;    // c에 a + b 결과 할당
```

세미콜론으로 구분하면 한 줄에 여러 개의 문을 사용할 수 있습니다.

###### 예제 3

```javascript
a = 5; b = 6; c = a + b;
```

{: .box-note}
웹에서 세미콜론이 없는 예를 볼 수 있습니다.<br>세미콜론으로 끝내는 것은 필수는 아니지만 강력히 권장합니다.

## JavaScript 공백

JavaScript는 여러 공백을 무시합니다. 스크립트를 읽기 쉽게 하기 위해 공백을 추가할 수 있습니다.

다음 행은 동일합니다.

###### 예제 4

```javascript
let person = "Hege";
let person="Hege";
```

연산자 주위에 공백을 두는 것이 좋습니다( ```=``` ```+``` ```-``` ```*``` ```/``` ).

###### 예제 5

```javascript
let x = y + z;
```

## JavaScript 행 길이 및 줄 바꿈

최고의 가독성을 위해 프로그래머들은 종종 80자를 넘는 코드 행을 피하는 것을 선호합니다.

JavaScript 문장이 한 줄에 맞지 않는 경우 연산자 뒤에서 줄 바꿈을 지정하는 것이 가장 좋습니다.

###### 예제 6

```javascript
document.getElementById("demo").innerHTML =
"Hello Dolly!";
```

## JavaScript 코드 블록

JavaScript 문장은 중괄호 ```{...}``` 안에 코드 블록으로 그룹화할 수 있습니다.

코드 블록의 목적은 함께 실행할 문을 정의하는 것입니다.

블록 단위로 그룹화된 문장은 JavaScript 함수에서 찾을 수 있습니다.

###### 예제 7

```javascript
function myFunction() {
  document.getElementById("demo1").innerHTML = "Hello Dolly!";
  document.getElementById("demo2").innerHTML = "How are you?";
}
```

## JavaScript 키워드

JavaScript 키워드는 예약어입니다. 예약된 단어는 변수의 이름으로 사용할 수 없습니다.

| 키워드 | 설명 |
| var | 변수 선언 |
| let | 블록 변수 선언 |
| const | 블록 상수 선언 |
| if | 조건에 따라 실행할 문장 블록 표시 |
| switch | 경우에 따라 실행할 문장 블록 표시 |
| for | 반복 실행할 문장 블록 표시 |
| function | 함수 선언 |
| return | 함수 탈출 |
| try | 문장 블록에 에러처리 핸들링 |
