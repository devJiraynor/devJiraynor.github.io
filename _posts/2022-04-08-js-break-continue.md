---
layout: post
title: JavaScript 42. Break문과 Continue문
subtitle: break 문은 반복문을 "점프 아웃"합니다. continue 문은 반복문에서 하나의 반복을 "점프"합니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript Break문과 Continue문

## break 문

```break```문을 이미 살펴보적이 있습니다. ```switch()``` 문의 "jump out"에 사용되었습니다.

```break```문은 반복문에서 벗어나는 데 사용할 수도 있습니다.

###### 예제 1

```javascript
for (let i = 0; i < 10; i++) {
  if (i === 3) { break; }
  text += "The number is " + i + "<br>";
}
```

위의 예에서 break 문은 반복 카운터(i)가 3일 때 반복문을 종료합니다.

## continue 문

continue 문은 지정된 조건이 발생하면 반복문에서 하나의 반복을 끊고 다음 반복을 계속합니다.

이 예에서는 3의 값을 생략합니다.

###### 예제 2

```javascript
for (let i = 0; i < 10; i++) {
  if (i === 3) { continue; }
  text += "The number is " + i + "<br>";
}
```

## label

레이블을 지정하려면 레이블 이름과 콜론을 사용하여 문장 앞에 배치합니다.

```javascript
label:
statements
```

```break``` 문과 ```continue``` 문은 코드 블록에서 "점프 아웃"할 수 있는 유일한 자바스크립트 문입니다.

구문 :

```javascript
break labelname;

continue labelname;
```

```continue``` 문(라벨 참조 포함 또는 없음)은 하나의 반복을 건너뛸 때만 사용할 수 있습니다.

```break``` 문은 레이블 참조 없이 루프 또는 스위치에서 점프하는 데만 사용할 수 있습니다.

레이블 참조를 사용하면 코드 블록에서 점프하는 데 ```break``` 문을 사용할 수 있습니다.

###### 예제 3

```javascript
const cars = ["BMW", "Volvo", "Saab", "Ford"];
list: {
  text += cars[0] + "<br>";
  text += cars[1] + "<br>";
  break list;
  text += cars[2] + "<br>";
  text += cars[3] + "<br>";
}
```

{: .box-note}
코드 블록은 ```{``` 와 ```}``` 사이의 코드 블록입니다.

