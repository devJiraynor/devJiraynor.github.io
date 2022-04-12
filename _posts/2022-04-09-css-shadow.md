---
layout: post
title: CSS 50. 그림자 효과 (Shadow Effects)
subtitle: CSS 그림자 효과 사용법에 대해 알아봅니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 그림자 효과

## 그림자 효과

CSS를 사용하여 텍스트와 요소에 그림자를 추가할 수 있습니다.

+ ```text-shadow```
+ ```box-shadow```

## 텍스트 그림자

```text-shadow``` 속성은 텍스트에 그림자를 적용합니다.

가장 간단하게는 수평 그림자(2px)와 수직 그림자(2px)만 지정할 수 있습니다.

###### 예제 1

```css
h1 {
  text-shadow: 2px 2px;
}
```

그림자에 색상을 추가합니다.

###### 예제 2

```css
h1 {
  text-shadow: 2px 2px red;
}
```

그림자에 흐릿한 효과를 추가합니다.

###### 예제 3

```css
h1 {
  text-shadow: 2px 2px 5px red;
}
```

검은색 그림자가 있는 흰색 텍스트를 보여 줍니다.

###### 예제 4

```css
h1 {
  color: white;
  text-shadow: 2px 2px 4px #000000;
}
```

빨간색 네온 야광 섀도우의 예입니다.

###### 예제 5

```css
h1 {
  text-shadow: 0 0 3px #FF0000;
}
```

## 다중 그림자

텍스트에 두 개 이상의 그림자를 추가하려면 쉼표로 구분된 그림자 목록을 추가할 수 있습니다.

다음은 빨간색과 파란색 네온 야광 섀도우의 예입니다.

###### 예제 6

```css
h1 {
  text-shadow: 0 0 3px #FF0000, 0 0 5px #0000FF;
}
```

다음 예제에서는 검은색, 파란색 및 어두운 파란색 그림자가 있는 흰색 텍스트를 보여 줍니다.

###### 예제 7

```css
h1 {
  color: white;
  text-shadow: 1px 1px 2px black, 0 0 25px blue, 0 0 5px darkblue;
}
```

```text-shadow``` 속성을 사용하여 그림자가 없는 일부 텍스트 주위에 일반 테두리를 만들 수 있습니다.

###### 예제 8

```css
h1 {
  color: coral;
  text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}
```

## box-shadow 속성

```box-shadow```은 하나 이상의 그림자를 요소에 적용하는 데 사용됩니다.

## 수평 수직 그림자 지정

가장 간단하게는 수평 및 수직 그림자만 지정할 수 있습니다. 그림자의 기본 색상은 현재 텍스트의 색입니다.

###### 예제 9

```css
div {
  box-shadow: 10px 10px;
}
```

## 그림자의 색상 지정

```color ``` 매개변수는 그림자의 색상을 정의합니다.

###### 예제 10

```css
div {
  box-shadow: 10px 10px lightblue;
}
```

## 그림자에 흐림 효과 추가

```blur``` 파라미터는 흐림도를 정의합니다. 수치가 높을수록 그림자가 더 흐려진다.

###### 예제 11

```css
div {
  box-shadow: 10px 10px 5px lightblue;
}
```

## 그림자 확산 반경 설정

```spread``` 매개 변수는 확산 반경을 정의합니다. 양의 값은 그림자 크기를 증가시키고 음의 값은 그림자 크기를 감소시킵니다.

###### 예제 12

```css
div {
  box-shadow: 10px 10px 5px 12px lightblue;
}
```

## 안쪽 그림자 설정

```inset``` 매개 변수는 그림자를 외부 그림자에서 내부 그림자로 변경합니다.

###### 예제 13

```css
div {
  box-shadow: 10px 10px 5px lightblue inset;
}
```

## 다중 그림자 추가

요소에는 여러 개의 그림자가 있을 수 있습니다.

```css
div {
  box-shadow: 5px 5px blue, 10px 10px red, 15px 15px green;
}
```

## 카드

```box-shadow``` 속성을 사용하여 종이와 같은 카드를 만들 수도 있습니다.

###### 예제 14

```css
div.card {
  width: 250px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  text-align: center;
}
```
