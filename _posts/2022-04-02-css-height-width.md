---
layout: post
title: CSS 11. 높이와 너비 (Height/Width)
subtitle: CSS height 및 width 속성은 요소의 높이 및 폭을 설정하기 위해 사용됩니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS Height, Width, Max-width

CSS ```height``` 및 ```width``` 속성은 요소의 높이 및 폭을 설정하기 위해 사용됩니다.

CSS ```max-width``` 속성은 요소의 최대 너비를 설정하기 위해 사용됩니다.

## 높이 및 너비 설정

```height``` 및 ```width``` 속성은 요소의 높이 및 너비를 설정하는 데 사용됩니다.

높이 및 너비 속성에는 패딩, 테두리 또는 여백이 포함되지 않습니다. 요소의 패딩, 테두리 및 여백 내부 영역의 높이/폭을 설정합니다.

## ```height```와 ```width``` 예제

<div style="height: 200px; width: 50%; background-color: powderblue;">이 요소는 높이 200px 너비 50%를 가집니다.</div> 

###### 예제 1

```css
div {
  height: 200px;
  width: 50%;
  background-color: powderblue;
}
```

<div style="height: 100px; width: 500px; background-color: powderblue;">이 요소는 높이 100px 너비 500px를 가집니다.</div> 

###### 예제 2

```css
div {
  height: 100px;
  width: 500px;
  background-color: powderblue;
}
```

**Note:** ```height``` 및 ```width``` 속성은 패딩, 테두리 또는 여백을 포함하지 않습니다! 요소의 패딩, 테두리 및 여백 안쪽 영역의 높이/폭을 설정합니다!

## max-width 설정

```max-width``` 속성은 요소의 최대 너비를 설정하는 데 사용됩니다.

```max-width```는 px, cm 등의 길이 값 또는 블록의 퍼센트(%)로 지정하거나 none으로 설정할 수 있습니다(기본값).

위의 ```<div>``` 문제는 브라우저 창이 요소의 폭(500px)보다 작을 때 발생합니다. 그런 다음 브라우저는 페이지에 수평 스크롤 막대를 추가합니다.

대신 ```max-width```를 사용하면 브라우저의 작은 창 처리 능력이 향상됩니다.

**Tip:** 브라우저 창을 500px보다 작은 폭으로 끌어 두 개의 div의 차이를 확인하십시오.

<div style="height: 100px; max-width: 500px; background-color: powderblue;">이 요소는 높이 100px 최대 너비 500px를 가집니다.</div> 

**Note:** 어떤 이유로 같은 요소에서 ```width``` 속성과 ```max-width``` 속성을 모두 사용하고 ```width``` 속성 값이 ```max-width``` 속성보다 클 경우 ```max-width``` 속성이 사용됩니다(```width``` 속성은 무시됩니다).

###### 예제 3

```css
div {
  max-width: 500px;
  height: 100px;
  background-color: powderblue;
}
```
