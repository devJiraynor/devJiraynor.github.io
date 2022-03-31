---
layout: post
title: JavaScript 07. 변수 (Variable)
subtitle: 변수는 데이터를 저장하기 위한 컨테이너입니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 변수

## 변수란?

변수는 데이터를 저장하기 위한 컨테이너입니다.

JavaScript 변수를 선언하는 4가지 방법:

+ ```var``` 사용
+ ```let``` 사용
+ ```const``` 사용
+ 아무것도 사용하지 않음

아래 예제의 ```x```, ```y``` 및 ```z```는 ```var``` 키워드로 선언된 변수입니다.

###### 예제 1

```javascript
var x = 5;
var y = 6;
var z = x + y;
```

아래 예제의 ```x```, ```y``` 및 ```z```는 ```let``` 키워드로 선언된 변수입니다.

###### 예제 2

```javascript
let x = 5;
let y = 6;
let z = x + y;
```

아래 예제의 ```x```, ```y``` 및 ```z```는 선언되지 않은 변수입니다.

###### 예제 3

```javascript
x = 5;
y = 6;
z = x + y;
```

위의 모든 예에서 다음을 추측할 수 있습니다.

+ ```x```는 값 5를 저장합니다.
+ ```y```는 값 6을 저장합니다.
+ ```z```는 값 11을 저장합니다.

{: .box_note}
<h4>JavaScript var를 사용하는 경우</h4><br>JavaScript 변수는 항상 ```var```, ```let``` 또는 ```const```로 선언합니다.<br>```var``` 키워드는 1995년부터 2015년까지 모든 JavaScript 코드에서 사용됩니다.<br>2015년에 JavaScript에 ```let``` 및 ```const``` 키워드가 추가되었습니다.<br>이전 브라우저에서 코드를 실행하려면 ```var```를 사용해야 합니다.
