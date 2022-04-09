---
layout: post
title: JavaScript 29. Date 형식 (Date Format)
subtitle: JavaScript의 Date Format에 대해서 알아봅니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript Date 형식

## 날짜 입력

JavaScript 날짜 입력 형식에는 일반적으로 세 가지 유형이 있습니다.

| **유형** |  **예** |
| ISO Date | "2015-03-25" |
| Short Date | "03/25/2015" |
| Long Date | 	"Mar 25 2015" or "25 Mar 2015" |

{: .box-note}
ISO 형식은 자바스크립트의 엄격한 표준을 따릅니다.<br>다른 형식들은 잘 정의되지 않았고 브라우저에 따라 다를 수 있습니다.

## 날짜 출력

입력 형식과 별개로 자바스크립트는 전체 텍스트 문자열 형식으로 날짜를 출력합니다.

## ISO Dates

ISO 8601은 날짜와 시간을 나타내는 국제 표준입니다.

ISO 8601 구문(YYY-MM-DD)도 자바스크립트 날짜 형식이 선호됩니다.

###### 예제 1

```javascript
const d = new Date("2015-03-25");
```

{: .box-note}
계산된 날짜는 사용자의 표준 시간대를 기준으로 합니다.<br>사용자의 시간대에 따라, 위의 결과는 3월 24일 또는 3월 25일 입니다.

## ISO Dates (연, 월)

ISO 날짜는 날짜를 지정하지 않고 쓸 수 있습니다(YYY-MM).

###### 예제 2

```javascript
const d = new Date("2015-03");
```

## ISO Dates (연도만)

ISO 날짜는 월과 일 없이 쓸 수 있습니다(YYYY).

###### 예제 3

```javascript
const d = new Date("2015");
```

## ISO Dates (날짜-시간)

ISO 날짜는 시간, 분, 초를 추가해서 쓸수 잇습니다(YYY-MM-DDTH:MM:SSZ)

###### 예제 4

```javsacript
const d = new Date("2015-03-25T12:00:00Z");
```

날짜와 시간은 대문자 T로 구분됩니다.

UTC 시간은 대문자 Z로 정의됩니다.

UTC를 기준으로 시간을 수정하려면 +HH:MM 또는 -HH:MM 대신에 Z를 제거하고 +HH를 추가합니다.

###### 예제 5

```javascript
const d = new Date("2015-03-25T12:00:00-06:30");
```

{: .box-note}
협정 세계시(UTC)는 그리니치 표준시와 동일합니다.

{: .box-danger}
날짜/시간 문자열에서 T 또는 Z를 생략하면 브라우저마다 다른 결과가 나타날 수 있습니다.

## 표준 시간대

날짜를 설정할 때 시간대를 지정하지 않고 JavaScript는 브라우저의 시간대를 사용합니다.

날짜를 가져올 때 시간대를 지정하지 않고 결과가 브라우저의 시간대로 변환됩니다.

즉, 날짜/시간이 GMT(그리니치 표준시)로 생성된 경우 사용자가 미국 중부 지역을 탐색하면 날짜/시간이 CDT(Central US Daylight Time)로 변환됩니다.

## Short Dates

짧은 날짜는 다음과 같이 "MM/DD/YYYY" 구문으로 작성됩니다.

###### 예제 6

```javascript
const d = new Date("03/25/2015");
```

## 경고

일부 브라우저에서는 선행 0이 없는 월 또는 일수가 오류를 발생시킬 수 있습니다.

```javascript
const d = new Date("2015-3-25");
```

"YYYY/MM/DD" 동작은 정의되지 않았습니다.

일부 브라우저는 형식을 추측하려고 합니다. ```NaN```을 반환하기도 합니다.

```javascript
const d = new Date("2015/03/25");
```

"DD-MM-YYYY" 동작은 정의되지 않았습니다.

일부 브라우저는 형식을 추측하려고 합니다. ```NaN```을 반환하기도 합니다.

```javascript
const d = new Date("25-03-2015");
```

## Long Dates

긴 날짜는 다음과 같은 "MM DD YYYYY" 구문으로 작성되는 경우가 많습니다.

###### 예제 7

```javascript
const d = new Date("Mar 25 2015");
```

월과 요일은 다음 순서로 지정할 수 있습니다.

###### 예제 8

```javascript
const d = new Date("25 Mar 2015");
```

달은 전체(January)로 쓸 수도 있고, 줄여서(Jan) 쓸 수도 있습니다.

###### 예제 9

```javascript
const d = new Date("January 25 2015");
```

###### 예제 10

```javascript
const d = new Date("Jan 25 2015");
```

쉼표는 무시됩니다. 이름은 대소문자를 구분하지 않습니다.

###### 예제 11

```javascript
const d = new Date("JANUARY, 25, 2015");
```

## 날짜 입력 - Date 파싱

유효한 날짜 문자열이 있는 경우 ```Date.parse()``` 메서드를 사용하여 밀리초로 변환할 수 있습니다.

```Date.parse()```는 1970년 1월 1일과 날짜 사이의 밀리초 수를 반환합니다.

###### 예제 12

```javascript
let msec = Date.parse("March 21, 2012");
```

밀리초 수를 사용하여 **날짜 객체로 변환**할 수 있습니다.

###### 예제 13

```javascript
let msec = Date.parse("March 21, 2012");
const d = new Date(msec);
```
