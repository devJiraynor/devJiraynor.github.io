---
layout: post
title: CSS 07. 배경 (Backgrounds)
subtitle: CSS 배경 속성은 요소의 배경 효과를 추가하기 위해 사용됩니다. 
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 배경

이 장에서는 다음 CSS 배경 속성에 대해 학습합니다.

+ ```background-color```
+ ```background-image```
+ ```background-repeat```
+ ```background-attachment```
+ ```background-position```
+ ```background```

## CSS background-color

```background-color``` 속성은 요소의 배경색을 지정합니다.

###### 예제 1

```css
body {
  background-color: lightblue;
}
```

CSS에서는 대부분의 경우 다음 항목에 의해 색상이 지정됩니다.

+ 색상 이름 (예: "red")
+ HEX 값 (예: "#ff0000")
+ RGB 값 (예: "rgb(255,0,0)")

## 다른 요소

임의의 HTML 요소의 배경색을 설정할 수 있습니다.

###### 예제 2

```css
h1 {
  background-color: green;
}

div {
  background-color: lightblue;
}

p {
  background-color: yellow;
}
```

## 불투명도/투명도

불투명도 속성은 요소의 불투명도/투명도를 지정합니다. 지정할 수 있는 값은 0.0 ~ 1.0입니다 값이 작을수록 투과성이 높아집니다.

###### 예제 3

```css
div {
  background-color: green;
  opacity: 0.3;
}
```

{: .box-note}
**Note:** 불투명도 속성을 사용하여 요소의 배경에 투명도를 추가할 경우 요소의 모든 하위 요소는 동일한 투명도를 상속합니다. 이렇게 하면 완전히 투명한 요소 내부의 텍스트를 읽기 어려울 수 있습니다.

## RGBA를 사용한 투명도

위의 예시와 같이 불투명도를 하위 요소에 적용하지 않으려면 RGBA 색상 값을 사용하십시오.

RGBA 색상 값은 rgba(red, green, blue, alpha)로 지정됩니다. 알파 매개 변수는 0.0(완전 투명)과 1.0(완전 불투명) 사이의 숫자입니다.

###### 예제4

```css
div {
  background: rgba(0, 128, 0, 0.3) 
}
```

## background-image

```background-image``` 속성은 요소의 배경으로 사용할 이미지를 지정합니다.

기본적으로는 이미지가 반복되어 전체 요소를 커버합니다.

###### 예제 5

```css
body {
  background-image: url("paper.gif");
}
```

{: .box-note}
**Note:** 배경 이미지를 사용할 때는 텍스트를 방해하지 않는 이미지를 사용하십시오.

```<p>``` 요소와 같은 특정 요소에 대해 배경 이미지를 설정할 수도 있습니다.

###### 예제 6

```css
p {
  background-image: url("paper.gif");
}
```

## background-repeat

기본적으로 ```background-image``` 속성은 이미지를 수평 및 수직 모두 반복합니다.

일부 이미지는 수평 또는 수직으로만 반복해야 합니다. 그렇지 않으면 다음과 같이 이상하게 표시됩니다.

###### 예제 7

```css
body {
  background-image: url("gradient_bg.png");
}
```

위 이미지가 수평으로만 반복되면(```background-repeat: repeat-x;```), 배경이 더 좋아집니다.

###### 예제 8

```css
body {
  background-image: url("gradient_bg.png");
  background-repeat: repeat-x;
}
```

{: .box-note}
**Tip:** 이미지를 수직으로 반복하려면 ```background-repeat: repeat-y;```를 설정합니다.

## background-repeat: no-repeat

배경 이미지를 한 번만 표시하는 것도 ```background-repeat``` 속성에 의해 지정됩니다.

###### 예제 9

```css
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
}
```

위의 예에서는 배경 이미지가 텍스트와 동일한 위치에 배치됩니다. 텍스트에 큰 지장을 주지 않도록 이미지의 위치를 변경해 주었으면 합니다.

## background-position

```background-position``` 속성은 배경 영상의 위치를 지정하는 데 사용됩니다.

###### 예제 10

```css
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
}
```
