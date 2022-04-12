---
layout: post
title: CSS 53. 2D 변환 (2D Transforms)
subtitle: CSS 2D 변환에 대해 알아봅니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 2D 변환

## 2D 변환

CSS 변환을 사용하면 요소를 이동, 회전, 축척 및 왜곡할 수 있습니다.

이 장에서는 다음 CSS 속성에 대해 학습합니다.

+ ```transform```

## 지원 브라우저

표의 숫자는 속성을 완전히 지원하는 최소 브라우저 버전을 지정합니다.

| 브라우저 | 구글 Chrome | 마이크로소프트 Edge | Firefox | Safari | Opera |
| 버전 | 36.0 | 10.0 | 16.0 | 9.0 | 23.0 |

## 2D 변환 메서드

```transform``` 속성을 사용하여 다음과 같은 2D 변환 방법을 사용할 수 있습니다.

+ ```translate()```
+ ```rotate()```
+ ```scaleX()```
+ ```scaleY()```
+ ```scale()```
+ ```skewX()```
+ ```skewY()```
+ ```skew()```
+ ```matrix()```

## translate()

```translate()``` 메서드는 X축과 Y축에 대해 주어진 매개변수에 따라 요소를 현재 위치에서 이동합니다.

다음 예제에서는 ```<div>``` 요소를 50픽셀 오른쪽으로 이동하고 현재 위치에서 100픽셀 아래로 이동합니다.

###### 예제 1

```css
div {
  transform: translate(50px, 100px);
}
```

## rotate()

```rotate()``` 메서드는 주어진 정도에 따라 요소를 시계 방향 또는 반시계 방향으로 회전시킵니다.

다음 예제에서는 ```<div>``` 요소를 시계 방향으로 20도 회전합니다.

###### 예제 2

```css
div {
  transform: rotate(20deg);
}
```

음수 값을 사용하면 요소가 시계 반대 방향으로 회전합니다.

다음 예제에서는 ```<div>``` 요소를 시계 반대 방향으로 20도 회전합니다.

###### 예제 3

```css
div {
  transform: rotate(-20deg);
}
```

## scale()

```scale()``` 메서드는 폭과 높이에 대해 주어진 모수에 따라 요소의 크기를 늘리거나 줄입니다.

다음 예제에서는 ```<div>``` 요소를 원래 너비의 두 배와 원래 높이의 세 배로 늘립니다.

###### 예제 4

```css
div {
  transform: scale(2, 3);
}
```

다음 예제에서는 ```<div>``` 요소를 원래 너비와 높이의 절반으로 줄입니다.

###### 예제 5

```css
div {
  transform: scale(0.5, 0.5);
}
```

## scaleX()

```scaleX()``` 메서드는 요소의 너비를 늘리거나 줄입니다.

다음 예제에서는 ```<div>``` 요소를 원래 너비의 두 배로 늘립니다.

###### 예제 6

```css
div {
  transform: scaleX(2);
}
```

다음 예제에서는 ```<div>``` 요소를 원래 너비의 절반으로 줄입니다.

###### 예제 7

```css
div {
  transform: scaleX(0.5);
}
```

## scaleY()

```scaleY()``` 메서드는 요소의 높이를 증가시키거나 감소시킵니다.

다음 예제에서는 ```<div>``` 요소를 원래 높이의 세 배로 늘립니다.

###### 예제 8

```css
div {
  transform: scaleY(3);
}
```

다음 예제에서는 ```<div>``` 요소를 원래 높이의 절반으로 줄입니다.

###### 예제 9

```css
div {
  transform: scaleY(0.5);
}
```

## skewX()

```skewX()``` 메서드는 X 축을 따라 지정된 각도만큼 요소를 왜곡시킵니다.

다음 예제에서는 ```<div>``` 요소를 X축을 따라 20도 기울입니다.

###### 예제 10

```css
div {
  transform: skewX(20deg);
}
```

## skewY()

```skewY()``` 메서드는 Y 축을 따라 지정된 각도만큼 요소를 스큐합니다.

다음 예제에서는 Y축을 따라 ```<div>``` 요소를 20도 기울입니다.

###### 예제 11

```css
div {
  transform: skewY(20deg);
}
```

## skew()

```skew()``` 메서드는 X 축과 Y 축을 따라 지정된 각도만큼 요소를 스큐합니다.

다음 예제에서는 ```<div>``` 요소를 X축을 따라 20도, Y축을 따라 10도 기울입니다.

###### 예제 12

```css
div {
  transform: skew(20deg, 10deg);
}
```

두 번째 매개 변수가 지정되지 않은 경우 값이 0입니다. 다음 예제에서는 ```<div>``` 요소를 X축을 따라 20도 기울입니다.

###### 예제 13

```css
div {
  transform: skew(20deg);
}
```

## matrix()

```matrix()``` 메서드는 모든 2D 변환 방법을 하나로 결합합니다.

```matrix()``` 메서드는는 회전, 스케일링, 이동(변환) 및 스큐 요소를 사용할 수 있는 수학적 함수가 포함된 6개의 모수가 사용됩니다.

매개변수는 ```matrix(scaleX(), skewY(), skewX(), scaleY(), translateX(), translateY())```입니다.

###### 예제 14

```css
div {
  transform: matrix(1, -0.3, 0, 1, 0, 0);
}
```
