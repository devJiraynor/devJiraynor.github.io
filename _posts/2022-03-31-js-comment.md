---
layout: post
title: JavaScript 06. 주석 (Commnet)
subtitle: JavaScript 주석은 JavaScript 코드를 설명하고 보다 읽기 쉽게 하기 위해 사용할 수 있습니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 주석

## 한 줄 주석

한 줄 주석은 ```//```로 시작합니다.

```//``` 와 행의 끝 사이의 텍스트는 JavaScript에 의해 무시됩니다(실행되지 않습니다).

다음 예제에서는 각 코드 행 앞에 한 줄의 주석을 사용합니다.

###### 예제 1

```javascript
// 헤딩 변경:
document.getElementById("myH").innerHTML = "My First Page";

// 문단 변경:
document.getElementById("myP").innerHTML = "My first paragraph.";
```

이 예에서는 각 행의 마지막에 한 줄 주석을 사용하여 설명합니다.

###### 예제 2

```javascript
let x = 5;      // x 를 선언하고 값으로 5를 할당
let y = x + 2;  // y 를 선언하고 값으로 x + 2를 할당
```

## 여러 줄 주석

여러 줄의 코멘트는 ```/*```로 시작하여 ```*/```로 끝납니다.

```/*``` ~ ```*/``` 사이의 텍스트는 JavaScript에 의해 무시됩니다.

다음 예제에서는 여러 줄의 주석(주석 블록)을 사용하여 코드를 설명합니다.

###### 예제 3

```javascript
/*
페이지 내에서
id가 myH인 헤딩과
id가 myP인 문단을
변경합니다.
*/
document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
```

{: .box-note}
보통 한 줄의 코멘트를 사용합니다.<br>블록 코멘트는 정식 문서에 자주 사용됩니다.

## 주석을 사용한 실행 방지

주석을 사용하여 코드 실행을 방지하여 코드 테스트를 진행할 수 있습니다.

코드 행 앞에 ```//```를 추가하면 코드 행이 실행 가능 행에서 주석으로 변경됩니다.

다음 예제에서는 ```//```를 사용하여 코드 행 중 하나가 실행되지 않도록 합니다.

###### 예제 4

```javascript
//document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
```

다음 예제에서는 주석 블록을 사용하여 여러 줄의 실행을 방지합니다.

###### 예제 5

```javascript
/*
document.getElementById("myH").innerHTML = "My First Page";
document.getElementById("myP").innerHTML = "My first paragraph.";
*/
```
