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

```css
div {
  background-color: green;
  opacity: 0.3;
}
```

{: .box-note}
**Note:**  불투명도 속성을 사용하여 요소의 배경에 투명도를 추가할 경우 요소의 모든 하위 요소는 동일한 투명도를 상속합니다. 이렇게 하면 완전히 투명한 요소 내부의 텍스트를 읽기 어려울 수 있습니다.
