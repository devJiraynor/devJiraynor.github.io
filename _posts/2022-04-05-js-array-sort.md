---
layout: post
title: JavaScript 25. 배열 정렬 (Array Sort)
subtitle: 배열을 정렬하는 방법에 대해 알아봅니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 배열 정렬

## 배열 정렬

```sort()``` 메서드는 배열을 알파벳 순으로 정렬합니다.

###### 예제 1

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort();
```

## 배열 역정렬

```reverse()``` 메서드는 배열의 요소를 반전시킵니다.

이 옵션을 사용하여 배열을 내림차순으로 정렬할 수 있습니다.

###### 예제 2

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort();
fruits.reverse();
```

## 숫자 정렬

기본적으로 ```sort()``` 함수는 값을 **문자열**로 정렬합니다.

이것은 문자열에서 잘 작동합니다("apple"은 "banana" 앞에 있다).

그러나 숫자를 문자열로 정렬하면 "25"는 "100"보다 크며, "2"는 "1"보다 앞에 나옵니다.

이 때문에 ```sort()``` 메서드는 숫자를 정렬할 때 잘못된 결과를 생성합니다.

**비교 함수**를 제공하여 이 문제를 해결할 수 있습니다.

###### 예제 3

```javascript
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return a - b});
```

배열 내림차순으로 정렬할 때도 동일한 방법을 사용합니다.

###### 예제 4

```javascript
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return b - a});
```

## 비교 함수

비교 함수의 목적은 대체 정렬 순서를 정의하는 것입니다.

비교 함수는 인수에 따라 음수, 0 또는 양의 값을 반환해야 합니다.

```javascript
function(a, b){return a - b}
```

```sort()``` 함수는 두 값을 비교할 때 값을 비교 함수로 보내고 반환된 값(음수, 0, 양수)에 따라 값을 정렬합니다.

결과가 음수 ```a```이면 ```b```보다 먼저 정렬됩니다.

결과가 양수 ```b```이면 ```a```보다 먼저 정렬됩니다.

결과가 0인 경우 두 값의 정렬 순서에 대한 변경은 수행되지 않습니다.

**예제**

비교 함수는 배열의 모든 값을 한 번에 두 개의 값 ```(a, b)```으로 비교합니다.

40과 100을 비교할 때 ```sort()``` 메서드는 비교 함수(40, 100)를 호출합니다.

함수는 40 - 100 ```(a - b)```을 계산하며, 결과는 음수(-60)이므로 정렬 함수는 40을 100보다 작은 값으로 정렬합니다.

이 코드 조각을 사용하여 숫자 및 알파벳 순으로 정렬하는 방법을 실험할 수 있습니다.

```html
<button onclick="myFunction1()">Sort Alphabetically</button>
<button onclick="myFunction2()">Sort Numerically</button>

<p id="demo"></p>

<script>
const points = [40, 100, 1, 5, 25, 10];
document.getElementById("demo").innerHTML = points;

function myFunction1() {
  points.sort();
  document.getElementById("demo").innerHTML = points;
}

function myFunction2() {
  points.sort(function(a, b){return a - b});
  document.getElementById("demo").innerHTML = points;
}
</script>
```

## 임의 순서로 배열 정렬

###### 예제 5

```javascript
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return 0.5 - Math.random()});
```

## Fisher Yates 방법

위의 예인 array.sort()는 정확하지 않습니다. 일부는 다른 방법을 사용합니다.

가장 인기 있는 정확한 방법은 Fisher Yates 셔플이라고 불리며, 1938년에 데이터 과학에 도입되었습니다!

자바스크립트에서 메소드는 다음과 같이 번역될 수 있다.

###### 예제 6

```javascript
const points = [40, 100, 1, 5, 25, 10];

for (let i = points.length -1; i > 0; i--) {
  let j = Math.floor(Math.random() * i)
  let k = points[i]
  points[i] = points[j]
  points[j] = k
}
```

## 가장 높은(또는 가장 낮은) 배열 값 찾기

배열에서 max 또는 min 값을 찾기 위한 기본 제공 함수는 없습니다.

그러나 배열을 정렬한 후에는 인덱스를 사용하여 가장 높은 값과 가장 낮은 값을 얻을 수 있습니다.

###### 오름차순 정렬:

```javascript
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return a - b});
// points[0]에 가장 낮은 값이 포함되고
// points[points.length-1]에 가장 높은 값이 포함됩니다.
```

###### 내림차순 정렬:

```javascript
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return b - a});
// points[0]에 가장 높은 값이 포함되고 
// points[points.length-1]에 가장 낮은 값이 포함됩니다.
```

{: .box-note}
가장 높은 값(또는 가장 낮은 값)만 찾으려는 경우 전체 배열을 정렬하는 것은 매우 비효율적인 방법입니다.

## 배열에서 Math.max() 사용

```Math.max.apply```를 사용하여 배열에서 가장 높은 숫자를 찾을 수 있습니다.

###### 예제 7

```javascript
function myArrayMax(arr) {
  return Math.max.apply(null, arr);
}
```

```Math.max.apply(null, [1, 2, 3])```는 ```Math.max(1, 2, 3)```와 동일합니다.

## 배열에서 Math.min() 사용

```Math.min.apply```를 사용하여 배열에서 가장 낮은 숫자를 찾을 수 있습니다.

###### 예제 8

```javascript
function myArrayMin(arr) {
  return Math.min.apply(null, arr);
}
```

```Math.min.apply(null, [1, 2, 3])```는 ```Math.min(1, 2, 3)```과 동일합니다.

## Min / Max 메서드 만들기

가장 빠른 해결책은 "수제" 방법을 사용하는 것이다.

이 함수는 각 값을 발견된 가장 높은 값과 비교하는 배열을 순환합니다.

###### 예제 9

```javascript
function myArrayMax(arr) {
  let len = arr.length;
  let max = -Infinity;
  while (len--) {
    if (arr[len] > max) {
      max = arr[len];
    }
  }
  return max;
}
```

이 함수는 각 값을 발견된 가장 낮은 값과 비교하는 배열을 순환합니다.

###### 예제 10

```javascript
function myArrayMin(arr) {
  let len = arr.length;
  let min = Infinity;
  while (len--) {
    if (arr[len] < min) {
      min = arr[len];
    }
  }
  return min;
}
```

## 배열 객체 정렬

자바스크립트 배열은 종종 다음과 같은 객체를 포함합니다.

###### 예제 11

```javascript
const cars = [
  {type:"Volvo", year:2016},
  {type:"Saab", year:2001},
  {type:"BMW", year:2010}
];
```

객체가 서로 다른 데이터 유형의 속성을 가지고 있더라도 ```sort()``` 메서드를 사용하여 배열을 정렬할 수 있습니다.

해결책은 비교 함수를 작성하여 속성 값을 비교하는 것입니다.

###### 예제 12

```javascript
cars.sort(function(a, b){return a.year - b.year});
```

문자열 속성을 비교하는 것은 조금 더 복잡합니다.

###### 예제 13

```javascript
cars.sort(function(a, b){
  let x = a.type.toLowerCase();
  let y = b.type.toLowerCase();
  if (x < y) {return -1;}
  if (x > y) {return 1;}
  return 0;
});
```
