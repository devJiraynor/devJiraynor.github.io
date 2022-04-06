---
layout: post
title: JavaScript 18. 문자열 메서드 (String )
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
