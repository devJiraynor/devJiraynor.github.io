---
layout: post
title: JavaScript 30. Date Set 메서드 (Date Set Method)
subtitle: date set 메서드는 날짜 객체에 정보를 설정하는 데 사용할 수 있습니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript Date Set 메서드

날짜 설정 방법을 사용하면 Date 객체에 대한 날짜 값(년, 월, 일, 시간, 분, 초, 밀리초)을 설정할 수 있습니다.

## Date Set 메서드

| **메서드** | **설명** |
| ```setDate()``` | 날짜를 숫자로 설정(1-31) |
| ```setFullYear()``` | 년도 설정(선택적으로 월 및 요일) |
| ```setHours()``` | 시간 설정(0-23) |
| ```setMilliseconds()``` | 밀리초 설정(0-999) |
| ```setMinutes()``` | 분 설정(0-59) |
| ```setMonth()``` | 월 설정(0-11) |
| ```setSeconds()``` | 초 설정(0-59) |
| ```setTime()``` | 시간 설정(1970년 1월 1일 이후 밀리초) |

## setFullYear() 메서드

```setFullYear()``` 메서드는 Date 객체의 연도를 설정합니다.

###### 예제 1

```javascript
const d = new Date();
d.setFullYear(2020);
```

```setFullYear()``` 메서드는 **선택적으로** 월과 요일을 설정할 수 있습니다.

###### 예제 2

```javascript
const d = new Date();
d.setFullYear(2020, 11, 3);
```

## setMonth() 메서드

```setMonth()``` 메서드는 Date 객체의 월(0-11)을 설정합니다.

###### 예제 3

```javascript
const d = new Date();
d.setMonth(11);
```

## setDate() 메서드

```setDate()``` 메서드는 Date 객체의 날짜(1-31)를 설정합니다.

###### 예제 4

```javascript
const d = new Date();
d.setDate(15);
```

```setDate()``` 메서드를 사용하여 Date 객체에 일 수를 추가할 수도 있습니다.

###### 예제 5

```javascript
const d = new Date();
d.setDate(d.getDate() + 50);
```

{: .box-note}
일 추가가 월 또는 연도를 변경하면 Date 객체에 의해 변경 사항이 자동으로 처리됩니다.

## setHours() 메서드

```setHours()``` 메서드는 Date 객체의 시간(0-23)을 설정합니다.

###### 예제 6

```javascript
const d = new Date();
d.setHours(22);
```

## setMinutes() 메서드

```setMinutes()``` 메서드는 Date 객체의 분(0-59)을 설정합니다.

###### 예제 7

```javascript
const d = new Date();
d.setMinutes(30);
```

## setSeconds() 메서드

```setSeconds()``` 메서드는 Date 객체의 초(0-59)를 설정합니다.

###### 예제 8

```javascript
const d = new Date();
d.setSeconds(30);
```

## 날짜 비교

날짜는 쉽게 비교할 수 있습니다.

다음 예제에서는 오늘 날짜를 2100년 1월 14일과 비교합니다.

###### 예제 9

```javascript
let text = "";
const today = new Date();
const someday = new Date();
someday.setFullYear(2100, 0, 14);

if (someday > today) {
  text = "Today is before January 14, 2100.";
} else {
  text = "Today is after January 14, 2100.";
}
```

{: .box-note}
JavaScript는 0에서 11까지의 달을 계산합니다. 1월은 0. 12월은 11입니다.

