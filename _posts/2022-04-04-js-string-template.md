---
layout: post
title: JavaScript 20. 문자열 템플릿 (String Template)
subtitle: 템플릿 리터럴은 내장된 표현식을 허용하는 문자열 리터럴입니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# Javascript 문자열 템플릿

## 백 틱 템플릿

**템플릿 리터럴**은 문자열을 정의하기 위해 따옴표(``` "" ```) 대신 역방향 체크(``` `` ```)를 사용합니다.

###### 예제 1

```javascript
let text = `Hello World!`;
```

## 문자열 내부의 따옴표

**템플릿 리터럴**을 사용하면 문자열 내에서 작은 따옴표와 큰 따옴표를 모두 사용할 수 있습니다.

```javascript
let text = `He's often called "Johnny"`;
```

## 여러 줄 문자열

```템플릿 리터럴```은 여러 줄 문자열을 허용합니다.

###### 예제 2

```javascript
let text =
`The quick
brown fox
jumps over
the lazy dog`;
```

## 보간법

```템플릿 리터럴```을 사용하면 변수와 식을 문자열로 쉽게 보간할 수 있습니다.

이 방법을 문자열 보간법이라고 합니다.

구문은 다음과 같습니다.

```javascript
${...}
```

## 변수 대체

```템플릿 리터럴```은 문자열에서 변수를 허용합니다.

###### 예제 3

```javascript
let firstName = "John";
let lastName = "Doe";

let text = `Welcome ${firstName}, ${lastName}!`;
```

{: .box-note}
변수를 실제 값으로 자동 대체하는 것을 **문자열 보간**이라고 합니다.

## 식 대체

```템플릿 리터럴```은 문자열로 표현식을 허용합니다.

###### 예제 4

```javascript
let price = 10;
let VAT = 0.25;

let total = `Total: ${(price * (1 + VAT)).toFixed(2)}`;
```

{: .box-note}
식을 실제 값으로 자동 대체하는 것을 **문자열 보간**이라고 합니다.

## HTML 템플릿

###### 예제 5

```javascript
let header = "Templates Literals";
let tags = ["template literals", "javascript", "es6"];

let html = `<h2>${header}</h2><ul>`;
for (const x of tags) {
  html += `<li>${x}</li>`;
}

html += `</ul>`;
```

## 지원 브라우저

```템플릿 리터럴```은 ES6 기능입니다(JavaScript 2015).

모든 최신 브라우저에서 지원됩니다.

```템플릿 리터럴```은 Internet Explorer에서 지원되지 않습니다.
