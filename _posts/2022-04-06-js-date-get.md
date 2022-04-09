---
layout: post
title: JavaScript 29. Date Get 메서드 (Date Get Method)
subtitle: date get 메서드는 날짜 객체에서 정보를 가져오는 데 사용할 수 있습니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript Date Get 메서드

| **메서드** | **설명** |
| ```getFullYear()``` | **연도**를 4자리 숫자로 가져오기(yyyy) |
| ```getMonth()``` | **월**을 숫자로 가져오기(0-11) |
| ```getDate()``` | **일**을 숫자로 가져오기(1-31). |
| ```getHours()``` | **시간** 가져오기(0-23) |
| ```getMinutes()``` | **분** 가져오기(0-59) |
| ```getSeconds()``` | **초** 가져오기(0-59) |
| ```getMilliseconds()``` | **밀리초** 가져오기(0-999) |
| ```getTime()``` | 시간 가져오기(1970년 1월 1일 이후 밀리초) |
| ```getDay()``` | 요일을 숫자로 가져오기(0-6) |
| ```Date.now()``` | 시간 가져오기 ECMAScript 5 |

## getTime() 메서드

```getTime()``` 메서드는 1970년 1월 1일 이후 밀리초 수를 반환합니다.

###### 예제 1

```javascript
const d = new Date();
d.getTime();
```

## getFullYear() 메서드

```getFullYear()``` 메서드는 날짜의 연도를 4자리 숫자로 반환합니다.

###### 예제 2

```javascript
const d = new Date();
d.getFullYear();
```

## getMonth() 메서드

```getMonth()``` 메서드는 날짜의 달을 숫자(0-11)로 반환합니다.

###### 예제 3

```javascript
const d = new Date();
d.getMonth();
```

{: .box-note}
자바스크립트에서 첫 번째 달(1월)은 0이므로 12월은 11을 반환합니다.

이름 배열을 사용하여 ```getMonth()```을 가져오면 해당 월을 이름으로 반환할 수 있습니다.

###### 예제 4

```javascript
const months = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];

const d = new Date();
let month = months[d.getMonth()];
```

## getDate() 메서드

```getDate()``` 메서드는 날짜의 날짜를 숫자(1-31)로 반환합니다.

###### 예제 5

```javascript
const d = new Date();
d.getDate();
```

## getHours() 메서드

```getHours()``` 메서드는 날짜의 시간을 숫자(0-23)로 반환합니다.

###### 예제 6

```javascript
const d = new Date();
d.getHours();
```

## getMinutes() 메서드

```getMinutes()``` 메서드는 날짜의 분을 숫자(0-59)로 반환합니다.

###### 예제 7

```javascript
const d = new Date();
d.getMinutes();
```

## getSeconds() 메서드

```getSeconds()``` 메서드는 날짜의 초를 숫자(0-59)로 반환합니다.

###### 예제 8

```javascript
const d = new Date();
d.getSeconds();
```

## getMilliseconds() 메서드

```getMilliseconds()``` 메서드는 날짜의 밀리초를 숫자(0-999)로 반환합니다.

###### 예제 7

```javascript
const d = new Date();
d.getMilliseconds();
```

## getDay() 메서드

```getDay()``` 메서드는 날짜의 요일을 숫자(0-6)로 반환합니다.

###### 예제 8

```javascript
const d = new Date();
d.getDay();
```

{: .box-note}
자바스크립트에서 주의 첫 번째 날 (0)은 "일요일"을 의미하며, 일부 국가에서는 주의 첫 날을 "월요일"로 간주하기도 합니다.

요일 이름 배열 및 ```getDay()```를 사용하여 요일을 이름으로 반환할 수 있습니다.

###### 예제 9

```javascript
const days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];

const d = new Date();
let day = days[d.getDay()];
```

