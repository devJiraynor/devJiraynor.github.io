---
layout: post
title: CSS 49. 그레이디언트 (Gradients)
subtitle: CSS 그레이디언트를 사용하면 두 개 이상의 지정된 색상 간에 매끄러운 전환을 표시할 수 있습니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 그레이디언트

CSS는 세 가지 유형의 그레이디언트를 정의합니다.

+ **Linear Gradient** (상-하/좌-우/대각선)
+ **Radial Gradient** (중심)
+ **Conic Gradient** (중앙을 기준으로 회전)

## Linear 그레이디언트

선형 그라디언트를 만들려면 두 개 이상의 색상 중지점을 정의해야 합니다. 색상 중지점은 부드러운 전환을 렌더링하려는 색상입니다. 그라데이션 효과와 함께 시작점과 방향(또는 각도)을 설정할 수도 있습니다.

#### 구문

```css
background-image: linear-gradient(direction, color-stop1, color-stop2, ...);
```

**상단에서 하단으로(기본값)**

다음 예제는 맨 위에서 시작하는 선형 그라데이션입니다. 빨간색에서 노란색으로 바뀝니다.

###### 예제 1

```css
#grad {
  background-image: linear-gradient(red, yellow);
}
```

**좌측에서 우측으로**

###### 예제 2

다음 예제는 왼쪽에서 시작하는 선형 그라데이션입니다. 빨간색에서 노란색으로 바뀝니다.

###### 예제 2

```css
#grad {
  background-image: linear-gradient(to right, red , yellow);
}
```

**대각선**

수평 및 수직 시작 위치를 모두 지정하여 대각선으로 그라데이션을 만들 수 있습니다.

다음 예제는 왼쪽 위에서 시작하여 오른쪽 아래로 이어지는 선형 그라데이션을 보여줍니다. 빨간색에서 노란색으로 바뀝니다.

###### 예제 3

```css
#grad {
  background-image: linear-gradient(to bottom right, red, yellow);
}
```

## 각도 사용

그라데이션의 방향을 더 많이 제어하려면 사전 정의된 방향(아래, 위, 오른쪽, 왼쪽, 아래 오른쪽 등) 대신 각도를 정의할 수 있습니다. 0deg 값은 "상단"과 같습니다. 90deg의 값은 "오른쪽"과 같습니다. 180deg의 값은 "하단"과 같습니다.

#### 구문

```css
background-image: linear-gradient(angle, color-stop1, color-stop2);
```

다음 예제에서는 선형 그라데이션에서 각도를 사용하는 방법을 보여 줍니다.

###### 예제 4

```css
#grad {
  background-image: linear-gradient(180deg, red, yellow);
}
```

## 다중 색상 중지점 사용

다음 예제에서는 여러 색상 중지점이 있는 선형 그라데이션(위에서 아래로)을 보여 줍니다.

###### 예제 5

```css
#grad {
  background-image: linear-gradient(red, yellow, green);
}
```

다음 예제에서는 레인보우 색상과 일부 텍스트를 사용하여 선형 그라데이션(왼쪽에서 오른쪽으로)을 작성하는 방법을 보여 줍니다.

###### 예제 6

```css
#grad {
  background-image: linear-gradient(to right, red,orange,yellow,green,blue,indigo,violet);
}
```

## 투명도 사용

그레이디언트는 페이딩 효과를 만드는 데 사용될 수 있는 투명성을 지원합니다.

투명도를 추가 위해 ```rgb()``` 함수를 사용하여 색상 정지점을 정의합니다. ```rgb()``` 함수의 마지막 매개 변수는 0에서 1까지의 값이 될 수 있으며, 색상의 투명도를 정의합니다. 0은 완전 투명도를 나타내고 1은 완전 색상(투명하지 않음)을 나타냅니다.

다음 예제는 왼쪽에서 시작하는 선형 그라데이션입니다. 완전히 투명하게 시작하여 전체 색상의 빨간색으로 바뀝니다.

###### 예제 7

```css
#grad {
  background-image: linear-gradient(to right, rgba(255,0,0,0), rgba(255,0,0,1));
}
```

## 선형 그라데이션 반복

```repeating-linear-gradient()``` 함수는 선형 그라데이션을 반복하는 데 사용됩니다.

###### 예제 8

```css
#grad {
  background-image: repeating-linear-gradient(red, yellow 10%, green 20%);
}
```

## Radial 그라디언트

방사형 그라데이션은 방사의 중심을 정의합니다.

방사형 그라데이션(radial gradient)을 만들려면 색상 정지점을 두 개 이상 정의해야 합니다.

#### 구문

```css
background-image: radial-gradient(shape size at position, start-color, ..., last-color);
```

**균일한 간격의 색상 중지점(기본값)**

다음 예제에서는 색상 중지점이 균일하게 간격을 두고 있는 방사형 그라데이션이 표시됩니다.

###### 예제 9

```css
#grad {
  background-image: radial-gradient(red, yellow, green);
}
```

**서로 다른 간격의 색상 중지점**

다음 예제에서는 색상 중지점 간격이 다른 방사형 그라데이션이 표시됩니다.

###### 예제 10

```css
#grad {
  background-image: radial-gradient(red 5%, yellow 15%, green 60%);
}
```

## 모양 설정

shape 매개변수는 모양을 정의합니다. 값 원 또는 타원을 사용할 수 있습니다. 기본값은 타원입니다.

다음 예제에서는 원의 모양을 가진 방사형 그라데이션을 보여 줍니다.

###### 예제 11

```css
#grad {
  background-image: radial-gradient(circle, red, yellow, green);
}
```

## 다른 크기의 키워드 사용

size 매개 변수는 그라데이션의 크기를 정의합니다. 다음 네 가지 값을 사용할 수 있습니다.

+ ```closest-side```
+ ```farthest-side```
+ ```closest-corner```
+ ```farthest-corner```

다음 예제는 키워드 크기가 다른 방사형 그라데이션입니다.

###### 예제 12

```css
#grad1 {
  background-image: radial-gradient(closest-side at 60% 55%, red, yellow, black);
}

#grad2 {
  background-image: radial-gradient(farthest-side at 60% 55%, red, yellow, black);
}
```

## 방사형 그라데이션 반복

```repeating-radial-gradient()```() 기능은 방사형 그라데이션을 반복하는 데 사용됩니다.

###### 예제 13

```css
#grad {
  background-image: repeating-radial-gradient(red, yellow 10%, green 15%);
}
```

## Conic 그라데이션

원뿔형 그라데이션은 중앙점을 중심으로 색 전환이 회전하는 그라데이션입니다.

원뿔형 그라데이션은 두 개 이상의 색상을 정의해야 합니다.

#### 구문

```css
background-image: conic-gradient([from angle] [at position,] color [degree], color [degree], ...);
```

기본적으로 각도는 0도이고 위치는 중앙입니다.

각도를 지정하지 않으면 색상이 중앙점 주위에 균등하게 분산됩니다.

## 3개 색상

다음 예제는 세 가지 색상의 원뿔 그라데이션입니다.

###### 예제 14

```css
#grad {
  background-image: conic-gradient(red, yellow, green);
}
```

## 5개 색상

다음 예제에서는 다섯 가지 색상의 원뿔 그라데이션이 표시됩니다.

###### 예제 15

```css
#grad {
  background-image: conic-gradient(red, yellow, green, blue, black);
}
```

## 3개 색상과 각도

다음 예제는 세 가지 색상과 각 색에 대한 각도를 가진 원뿔 그라데이션입니다.

###### 예제 16

```css
#grad {
  background-image: conic-gradient(red 45deg, yellow 90deg, green 210deg);
}
```

## 파이 차트형 그라데이션

```border-radius: 50%```를 추가하면 원뿔형 그라데이션이 파이처럼 보입니다.

###### 예제 17

```css
#grad {
  background-image: conic-gradient(red, yellow, green, blue, black);
  border-radius: 50%;
}
```

다음은 모든 색에 대해 정의된 도수를 가진 또 다른 파이 차트입니다.

###### 예제 18

```css
#grad {
  background-image: conic-gradient(red 0deg, red 90deg, yellow 90deg, yellow 180deg, green 180deg, green 270deg, blue 270deg);
  border-radius: 50%;
}
```

## 각도가 지정된 원뿔형 그라데이션

```[from angle]```은 전체 원뿔 그라데이션이 회전하는 각도를 지정합니다.

다음 예제는 각도가 90도인 원뿔 그라데이션을 보여줍니다.

###### 예제 19

```css
#grad {
  background-image: conic-gradient(from 90deg, red, yellow, green);
}
```

## 지정된 중심 위치를 사용한 원뿔 그라데이션

```[at position]```은 원뿔 그라데이션의 중심을 지정합니다.

다음 예제에서는 중심 위치가 60% 45%인 원뿔 그라데이션을 보여 줍니다.

###### 예제 20

```css
#grad {
  background-image: conic-gradient(at 60% 45%, red, yellow, green);
}
```

## 원뿔 그라데이션 반복

```repeating-conic-gradient()``` 함수는 원뿔 그라데이션을 반복하는 데 사용됩니다.

###### 예제 21

```css
#grad {
  background-image: repeating-conic-gradient(red 10%, yellow 20%);
  border-radius: 50%;
}
```

다음은 정의된 색상 시작점 및 색상 중지점을 사용한 반복 원뿔 그라데이션입니다.

###### 예제 22

```css
#grad {
  background-image: repeating-conic-gradient(red 0deg 10deg, yellow 10deg 20deg, blue 20deg 30deg);
  border-radius: 50%;
}
```
