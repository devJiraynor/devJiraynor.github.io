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

{: .box-note}
<h4>JavaScript ```var```를 사용하는 경우</h4>JavaScript 변수는 항상 ```var```, ```let``` 또는 ```const```로 선언합니다.<br>```var``` 키워드는 1995년부터 2015년까지 모든 JavaScript 코드에서 사용됩니다.<br>2015년에 JavaScript에 ```let``` 및 ```const``` 키워드가 추가되었습니다.<br>이전 브라우저에서 코드를 실행하려면 ```var```를 사용해야 합니다.

## JavaScript ```const```를 사용하는 경우

일반 규칙을 사용하는 경우: 항상 변수를 ```const```로 선언합니다.

변수 값이 변경될 수 있다고 생각되면 ```let```을 사용하십시오.

이 예에서는 ```price1```, ```price2``` 및 ```total```이 변수입니다.

###### 예제 4

```javascript
const price1 = 5;
const price2 = 6;
let total = price1 + price2;
```

두 변수 ```price1```과 ```price2```는 ```const``` 키워드로 선언됩니다.

이들은 상수 값이며 변경할 수 없습니다.

변수 ```total```은 ```let``` 키워드로 선언됩니다.

이것은 변경할 수 있는 값입니다.

## 대수학

대수학에서와 마찬가지로 변수는 값을 유지합니다.

```javascript
let x = 5;
let y = 6;
```

대수학에서와 마찬가지로 변수는 식에 사용됩니다.

```javascript
let z = x + y;
```

위의 예에서 합계가 11로 계산되었음을 알 수 있습니다.

{: .box-note}
변수는 값을 저장하기 위한 컨테이너입니다.

## JavaScript 식별자

모든 JavaScript **변수**는 **고유한 이름**으로 **식별**되어야 합니다.

이러한 고유 이름을 **식별자**라고 합니다.

식별자는 짧은 이름(x 및 y 등)이거나 보다 알기 쉬운 이름(age, sum, totalVolume)일 수 있습니다.

변수의 이름(고유 식별자)을 작성하기 위한 일반적인 규칙은 다음과 같습니다.

+ 이름에는 문자, 숫자, 밑줄 및 달러 기호를 포함할 수 있습니다.
+ 이름은 문자로 시작해야 합니다.
+ 이름은 ```$```와 ```_```로 시작할 수 있습니다.
+ 이름은 대소문자를 구분합니다(y와 Y는 다른 변수입니다).
+ 예약된 단어(예: JavaScript 키워드)는 이름으로 사용할 수 없습니다.

{: box-note}
JavaScript 식별자는 대소문자를 구분합니다.

## 할당 연산자

JavaScript에서 등호(```=```)는 "같음" 연산자가 아니라 "할당" 연산자입니다.

이것은 대수학과는 다릅니다. 대수학에서는 다음 사항이 의미가 없습니다.

```javascript
x = x + 5
```

그러나 JavaScript에서는 x + 5의 값을 x에 할당하는 것이 매우 당연합니다.

(x + 5의 값을 계산하여 결과를 x에 넣습니다. x 값은 5씩 증가합니다).

{: .box-note}
JavaScript에서 "같음" 연산자는 ```==```로 작성됩니다.

## JavaScript 데이터 타입

JavaScript 변수는 100과 같은 숫자와 "John Doe"와 같은 텍스트 값을 포함할 수 있습니다.

프로그래밍에서 텍스트 값은 텍스트 문자열이라고 합니다.

JavaScript는 많은 종류의 데이터를 처리할 수 있지만, 지금은 숫자와 문자열만 생각해 보세요.

문자열은 큰따옴표 또는 작은따옴표 안에 씁니다. 숫자는 따옴표 없이 씁니다.

따옴표 안에 숫자를 넣으면 텍스트 문자열로 처리됩니다.

###### 예제 5

```javascript
const pi = 3.14;
let person = "John Doe";
let answer = 'Yes I am!';
```

## JavaScript 변수 선언

JavaScript에서 변수를 만드는 것을 변수 선언이라고 합니다.

JavaScript 변수는 ```var``` 또는 ```let``` 키워드를 사용하여 선언합니다.

```javascript
var carName;
```

또는

```javascript
let carName;
```

선언 후 변수는 값을 갖지 않습니다(```undefined``` 상태).

변수에 값을 **할당**하려면 등호를 사용합니다.

```javascript
carName = 'Volvo';
```

변수를 선언할 때 변수에 값을 할당할 수도 있습니다.

```javascript
let carName = 'Volvo';
```

다음 예제에서는 ```carName```이라는 변수를 만들고 "Volvo" 값을 할당합니다.

그런 다음 id="demo"로 HTML 단락 내의 값을 "출력"합니다.

###### 예제 6

```html
<p id="demo"></p>

<script>
let carName = "Volvo";
document.getElementById("demo").innerHTML = carName;
</script>
```

{: .box-note}
**Note:** 스크립트 시작 부분에서 모든 변수를 선언하는 것이 좋습니다.

## 하나의 문장으로 여러 변수 선언

하나의 문장에 여러 변수를 선언할 수 있습니다.

문장을 ```let```으로 시작하고 변수를 ```,```로 구분합니다.

###### 예제 7

```javascript
let person = "John Doe", carName = "Volvo", price = 200;
```

선언은 여러 행에 걸쳐 있을 수 있습니다.

###### 예제 8

```javascript
let person = "John Doe",
carName = "Volvo",
price = 200;
```

## 값 = ```undefined```

컴퓨터 프로그램에서는 변수가 값 없이 선언되는 경우가 많습니다. 값은 계산해야 하는 값일 수도 있고 사용자 입력과 같이 나중에 제공될 값일 수도 있습니다.

값을 지정하지 않고 선언된 변수는 값을 ```undefined```라 합니다.

변수 ```carName```은 다음 문장 실행 후 값은 ```undefined``` 입니다.

###### 예제 9

```javascript
let carName;
```

## JavaScript 변수 재선언

```var```로 선언된 JavaScript 변수를 다시 선언해도 값이 손실되지 않습니다.

변수 ```carName```은 다음 문을 실행한 후에도 값 "Volvo"를 유지합니다.

###### 예제 10

```javascript
var carName = "Volvo";
var carName;
```

{: .box-note}
**Note:** let 또는 const로 선언된 변수는 다시 선언할 수 없습니다.

## JavaScript 산술

대수학과 마찬가지로 ```=``` 및 ```+``` 와 같은 연산자를 사용하여 JavaScript 변수를 사용하여 산술할 수 있습니다.

###### 예제 11

```javascript
let x = 5 + 2 + 3;
```

문자열을 더할할 수도 있지만 문자열은 연결됩니다.

###### 예제 12

```javascript
let x = "John" + " " + "Doe";
```

아래 문장을 실행해보세요.

###### 예제 13

```javascript
let x = "5" + 2 + 3;
```

{: .box-note}
**Note:** 따옴표 안에 숫자를 넣으면 나머지 숫자는 문자열로 처리되어 연결됩니다.

아래 문장을 실행해보세요.

###### 예제 14

```javascript
let x = 2 + 3 + "5";
```

## JavaScript 달러 기호 ```$```

JavaScript는 ```$``` 기호를 문자로 취급하므로 ```$```를 포함하는 식별자는 유효한 변수 이름입니다.

###### 예제 15

```javascript
let $ = "Hello World";
let $$$ = 2;
let $myMoney = 5;
```

달러 기호를 사용하는 것은 JavaScript에서는 그다지 흔하지 않지만 전문 프로그래머들은 종종 자바스크립트 라이브러리의 주요 함수의 별칭으로 사용합니다.

예를 들어 JavaScript 라이브러리 jQuery에서는 HTML 요소를 선택하기 위해 주요 함수 ```$```가 사용됩니다. jQuery ```$("p");```는 "모든 p 요소 선택"을 의미합니다.

## JavaScript 밑줄 ```_```

JavaScript는 밑줄을 문자로 처리하므로 ```_```를 포함하는 식별자는 다음과 같은 유효한 변수 이름입니다.

###### 예제 16

```javascript
let _lastName = "Johnson";
let _x = 2;
let _100 = 5;
```

JavaScript에서는 언더스코어를 사용하는 것이 일반적이지 않지만 전문 프로그래머들 사이에서는 이를 "private(hidden)" 변수의 별칭으로 사용하는 것이 관례입니다.
