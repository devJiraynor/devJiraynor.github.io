---
layout: post
title: CSS 13. Outline
subtitle: 아웃라인은 요소의 테두리 외부에 그려진 선입니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS Outline

## Outline

아웃라인은 요소를 "눈에 띄게" 하기 위해 요소 주위에 그려진 선입니다.

<img src="https://raw.githubusercontent.com/devJiraynor/devJiraynor.github.io/master/assets/img/css/css_outline_01.PNG">

CSS에는 다음 outline 속성이 있습니다.

+ ```outline-style```
+ ```outline-color```
+ ```outline-width```
+ ```outline-offset```
+ ```outline```

{: .box-note}
**Note:** 아웃라인은 테두리와 다릅니다! 테두리와 달리 아웃라인은 요소의 테두리 외부에 그려지며 다른 내용과 겹칠 수 있습니다. 또한 아웃라인은 요소의 치수에 포함되지 않습니다. 요소의 전체 폭과 높이는 아웃라인의 폭에 영향을 받지 않습니다.

## Outline Style

```outline-style``` 속성은 아웃라인의 스타일을 지정하며 다음 값 중 하나를 가질 수 있습니다.

+ ```dotted``` - 점선 아웃라인을 정의합니다.
+ ```dashed``` - 점선 아웃라인을 정의합니다.
+ ```solid``` - 실선 아웃라인을 정의합니다.
+ ```double``` - 이중 실선 아웃라인을 정의합니다.
+ ```groove``` - 3D 홈 아웃라인을 정의합니다.
+ ```ridge``` - 3D 테두리 아웃라인을 정의합니다.
+ ```inset``` - 3D 오목 아웃라인을 정의합니다.
+ ```outset``` - 3D 볼록 아웃라인을 정의합니다.
+ ```none``` - 아웃라인을 정의하지 않습니다.
+ ```hidden``` - 아웃라인을 숨깁니다.

###### 예제 1

```css
p.dotted {outline-style: dotted;}
p.dashed {outline-style: dashed;}
p.solid {outline-style: solid;}
p.double {outline-style: double;}
p.groove {outline-style: groove;}
p.ridge {outline-style: ridge;}
p.inset {outline-style: inset;}
p.outset {outline-style: outset;}
```

결과 : 

<p style="outline-style: dotted;">점선 아웃라인을 정의합니다.</p>
<p style="outline-style: dashed;">점선 아웃라인을 정의합니다.</p>
<p style="outline-style: solid;">실선 아웃라인을 정의합니다.</p>
<p style="outline-style: double;">이중 실선 아웃라인을 정의합니다.</p>
<p style="outline-style: groove;">3D 홈 아웃라인을 정의합니다.</p>
<p style="outline-style: ridge;">3D 테두리 아웃라인을 정의합니다.</p>
<p style="outline-style: inset;">3D 오목 아웃라인을 정의합니다.</p>
<p style="outline-style: outset;">3D 볼록 아웃라인을 정의합니다.</p>

{: .box-note}
**Note:** ```outline-style``` 속성이 설정되지 않는 한 다른 아웃라인 속성은 아무 효과도 없습니다.

## outline width

```outline-width``` 속성은 아웃라인의 너비를 지정하고 다음 값 중 하나를 지정할 수 있습니다.

+ thin (1px)
+ medium (3px)
+ thick ( 5px)
+ 특정 사이즈 (in, px, pt, cm, em 등)

###### 예제 2

```css
p.ex1 {
  border: 1px solid black;
  outline-style: solid;
  outline-color: red;
  outline-width: thin;
}

p.ex2 {
  border: 1px solid black;
  outline-style: solid;
  outline-color: red;
  outline-width: medium;
}

p.ex3 {
  border: 1px solid black;
  outline-style: solid;
  outline-color: red;
  outline-width: thick;
}

p.ex4 {
  border: 1px solid black;
  outline-style: solid;
  outline-color: red;
  outline-width: 4px;
}
```

## outline color

```outline-color``` 속성은 아웃라인의 색상을 설정하는 데 사용됩니다.

색상은 다음과 같이 설정할 수 있습니다.

+ 이름 - "red"과 같은 색상 이름을 지정합니다.
+ HEX - "#ff0000"과 같은 16진수 값을 지정합니다.
+ RGB - "rgb(255,0,0)"와 같은 RGB 값을 지정합니다.
+ HSL - "hsl(0, 100%, 50%)"와 같은 HSL 값을 지정합니다.
+ 반전 - 색상 반전 수행(색 배경에 관계없이 윤곽선이 표시되도록 함)

###### 예제 3

```css
p.ex1 {
  border: 2px solid black;
  outline-style: solid;
  outline-color: red;
}

p.ex2 {
  border: 2px solid black;
  outline-style: dotted;
  outline-color: blue;
}

p.ex3 {
  border: 2px solid black;
  outline-style: outset;
  outline-color: grey;
}
```

## HEX 값

아웃라인 색상은 16진수 값(HEX)을 사용하여 지정할 수도 있습니다.

###### 예제 4

```css
p.ex1 {
  outline-style: solid;
  outline-color: #ff0000; /* red */
}
```

## RGB 값

아웃라인 색상은 RGB 값을 사용하여 지정할 수도 있습니다.

###### 예제 5

```css
p.ex1 {
  outline-style: solid;
  outline-color: rgb(255, 0, 0); /* red */
}
```

## HSL 값

아웃라인 색상은 HSL 값을 사용하여 지정할 수도 있습니다.

###### 예제 6

```css
p.ex1 {
  outline-style: solid;
  outline-color: hsl(0, 100%, 50%); /* red */
}
```

## outline - 축약 속성

```outline``` 속성은 다음과 같은 개별 아웃라인 속성을 설정하기 위한 축약 속성입니다.

+ ```outline-width```
+ ```outline-style``` (필수)
+ ```outline-color```

```outline``` 속성은 위의 목록에서 1~3 개의 값으로 지정됩니다. 값의 순서는 중요하지 않습니다.

###### 예제 7

```css
p.ex1 {outline: dashed;}
p.ex2 {outline: dotted red;}
p.ex3 {outline: 5px solid yellow;}
p.ex4 {outline: thick ridge pink;}
```

## outline offset

```outline-offset``` 속성은 요소의 외곽선과 가장자리/테두리 사이에 공간을 추가합니다. 요소와 그 윤곽선 사이의 공간은 투명합니다.

###### 예제 8

```css
p {
  margin: 30px;
  border: 1px solid black;
  outline: 1px solid red;
  outline-offset: 15px;
}
```
