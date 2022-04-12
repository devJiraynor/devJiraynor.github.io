---
layout: post
title: CSS 48. 색상 키워드 (color Keyword)
subtitle: transparent, currentcolor 및 inherit  키워드에 대해 설명합니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 색상 키워드

## transparent 키워드

```transparent``` 키워드는 색상을 투명하게 만드는 데 사용됩니다. 요소의 투명한 배경색을 만드는 데 자주 사용됩니다.

###### 예제 1 - ```<div>``` 요소의 배경색이 완전히 투명해지고 배경 이미지가 다음을 통해 표시됩니다.

```css
body {
  background-image: url("paper.gif");
}

div {
  background-color: transparent;
}
```

{: .box-note}
```transparent``` 키워드는 rgba(0,0,0,0)와 같습니다. RGBA 색상 값은 색상의 불투명도를 지정하는 알파 채널로 RGB 색상 값을 확장한 것입니다.

## currentcolor 키워드

```currentcolor``` 키워드는 요소의 색상 속성의 현재 값을 유지하는 변수와 같습니다.

이 키워드는 요소 또는 페이지에서 특정 색상을 일치시키려면 유용합니다.

###### 예제 2 - ```<div>``` 요소의 텍스트 색상이 파란색이기 때문에 ```<div>``` 요소의 테두리 색상이 파란색이 됩니다.

```css
div {
  color: blue;
  border: 10px solid currentcolor;
}
```

###### 예제 3 - ```<div>```의 배경색이 차체 요소의 현재 색상 값으로 설정됩니다.

```css
body {
  color: purple;
}

div {
  background-color: currentcolor;
}
```

###### 예제 4 - ```<div>```의 테두리 색상과 섀도 색상이 신체 요소의 현재 색상 값으로 설정됩니다.

```css
body {
 color: green;
}

div {
  box-shadow: 0px 0px 15px currentcolor;
  border: 5px solid currentcolor;
}
```

## inherit 키워드

```inherit``` 키워드는 속성이 상위 요소에서 해당 값을 상속하도록 지정합니다.

```inherit``` 키워드는 모든 CSS 속성과 HTML 요소에 사용할 수 있습니다.

###### 예제 5 - ```<span>```의 테두리 설정은 상위 요소에서 상속됩니다.

```css
div {
  border: 2px solid red;
}

span {
  border: inherit;
}
```
