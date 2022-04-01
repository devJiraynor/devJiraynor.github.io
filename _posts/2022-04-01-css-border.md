---
layout: post
title: CSS 08. 테두리 (Borders)
subtitle: CSS 테두리 특성을 사용하여 요소의 테두리 스타일, 너비 및 색상을 지정할 수 있습니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 테두리

## border-style

```border-style``` 속성은 표시할 테두리 유형을 지정합니다.

다음 값이 허용됩니다.

+ ```dotted``` - 점선 테두리를 정의합니다.
+ ```dashed``` - 점선 테두리를 정의합니다.
+ ```solid``` - 실선 테두리를 정의합니다.
+ ```double``` - 이중 테두리를 정의합니다.
+ ```groove``` - 3D 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.
+ ```ridge``` - 3D 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.
+ ```inset``` - 3D 오록 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.
+ ```outset``` - 3D 볼목 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.
+ ```none``` - 테두리를 정의하지 않습니다.
+ ```hidden``` - 테두리를 숨깁니다.

###### 예제 1

```css
p.dotted {border-style: dotted;}
p.dashed {border-style: dashed;}
p.solid {border-style: solid;}
p.double {border-style: double;}
p.groove {border-style: groove;}
p.ridge {border-style: ridge;}
p.inset {border-style: inset;}
p.outset {border-style: outset;}
p.none {border-style: none;}
p.hidden {border-style: hidden;}
p.mix {border-style: dotted dashed solid double;}
```

결과 : 

<p style="border-style: dotted;">점선 테두리를 정의합니다.</p>
<p style="border-style: dashed;">점선 테두리를 정의합니다.</p>
<p style="border-style: solid;">실선 테두리를 정의합니다.</p>
<p style="border-style: double;">이중 테두리를 정의합니다.</p>
<p style="border-style: groove;">3D 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.</p>
<p style="border-style: ridge;">3D 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.</p>
<p style="border-style: inset;">3D 오목 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.</p>
<p style="border-style: outset;">3D 볼록 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.</p>
<p style="border-style: none;">테두리를 정의하지 않습니다.</p>
<p style="border-style: hidden;">테두리를 숨깁니다.</p>
<p style="border-style: dotted dashed solid double;">스타일을 섞습니다.</p>

{: .box-note}
**Note:** ```border-style``` 속성이 설정되지 않는 한 다른 CSS 테두리 속성은 아무 효과도 없습니다.

## border-width

```border-width``` 속성은 네 개의 테두리 너비를 지정합니다.

폭은 특정 크기(px, pt, cm, em 등)로 설정하거나 세 가지 사전 정의된 값(thin, medium, thick) 중 하나를 사용하여 설정할 수 있습니다.

###### 예제 2

```css
p.one {
  border-style: solid;
  border-width: 5px;
}

p.two {
  border-style: solid;
  border-width: medium;
}

p.three {
  border-style: dotted;
  border-width: 2px;
}

p.four {
  border-style: dotted;
  border-width: thick;
}
```

결과:

<p style="border-style: solid; border-width: 5px;">5px border-width</p>
<p style="border-style: solid; border-width: medium;">medium border-width</p>
<p style="border-style: dotted; border-width: 2px;">2px border-width</p>
<p style="border-style: dotted; border-width: thick;">thick border-width</p>

## 특정 측면 너비

```border-width``` 속성에는 1~4개의 값을 지정할 수 있습니다(위 테두리, 오른쪽 테두리, 아래쪽 테두리 및 왼쪽 테두리).

###### 예제 3

```css
p.one {
  border-style: solid;
  border-width: 5px 20px; /* 상하 5px, 측면 20px */
}

p.two {
  border-style: solid;
  border-width: 20px 5px; /* 상하 20px, 측면 5px */
}

p.three {
  border-style: solid;
  border-width: 25px 10px 4px 35px; /* 상단 25px, 우측 10px, 하단 4px, 좌측 35px */
}
```

## border-color

```border-color``` 속성은 네 개의 테두리 색상을 설정하는 데 사용됩니다.

색상은 다음과 같이 설정할 수 있습니다.

+ 이름 - "red"와 같은 색상 이름을 지정합니다.
+ HEX - "#ff0000"과 같은 16진수 값을 지정합니다.
+ RGB - "rgb(255,0,0)"와 같은 RGB 값을 지정합니다.
+ HSL - "hsl(0, 100%, 50%)"와 같은 HSL 값을 지정합니다.
+ 투명도

**Note:** ```border-color```가 설정되지 않은 경우 요소의 색상을 상속합니다.

###### 예제 4

```css
p.one {
  border-style: solid;
  border-color: red;
}

p.two {
  border-style: solid;
  border-color: green;
}

p.three {
  border-style: dotted;
  border-color: blue;
}
```

결과 :

<p style="border-style: solid; border-color: red;">빨간 테두리</p>
<p style="border-style: solid; border-color: green;">초록 테두리</p>
<p style="border-style: dotted;  border-color: blue;">파란 테두리</p>

## 특정 측면 색상

```border-color``` 속성에는 1~4개의 값을 지정할 수 있습니다(위 테두리, 오른쪽 테두리, 아래쪽 테두리 및 왼쪽 테두리).

###### 예제 5

```css
p.one {
  border-style: solid;
  border-color: red green blue yellow; /* 빨간색 상단, 녹색 오른쪽, 파란색 하단 및 노란색 왼쪽 */
}
```

## HEX 값

테두리 색상은 16진수 값(HEX)을 사용하여 지정할 수도 있습니다.

###### 예제 6

```css
p.one {
  border-style: solid;
  border-color: #ff0000; /* red */
}
```

## RGB 값

테두리 색상은 RGB 값을 사용하여 지정할 수도 있습니다.

###### 예제 7

```css
p.one {
  border-style: solid;
  border-color: rgb(255, 0, 0); /* red */
}
```

## HSL 값

테두리 색상은 HSL 값을 사용하여 지정할 수도 있습니다.

###### 예제 8

```css
p.one {
  border-style: solid;
  border-color: hsl(0, 100%, 50%); /* red */
}
```

## 개별 측면 테두리

CSS 에는 각 테두리(상단, 오른쪽, 하단, 및 왼쪽)를 지정하는 속성도 있습니다.

###### 예제 9

```css
p {
  border-top-style: dotted;
  border-right-style: solid;
  border-bottom-style: dotted;
  border-left-style: solid;
}
```

결과 : 

<p style="border-top-style: dotted; border-right-style: solid; border-bottom-style: dotted; border-left-style: solid;">각기 다른 테두리 스타일</p>

위의 예에서는 아래와 같은 결과를 얻을 수 있습니다.

###### 예제 10

```css
p {
  border-style: dotted solid;
}
```

동작은 다음과 같습니다.

```border-style``` 속성의 값이 4개인 경우:

+ **border-style: dotted solid double dashed;**
- 상단 테두리 점선
- 오른쪽 테두리 실선
- 하단 테두리 이중
- 왼쪽 테두리 점선

```border-style``` 속성값이 3개인 경우:

+ **border-style: dotted solid double;**
- 상단 테두리 점선
- 좌우 테두리 실선
- 하단 테두리 이중

```border-style``` 속성값이 2개인 경우:

+ **border-style: dotted solid;**
- 상하 테두리 점선
- 좌우 테두리 실선

```border-style``` 속성값이 1개인 경우:

+ **border-style: dotted;**
- 모든 테두리 점선

###### 예제 11

```css
/* 4개 값 */
p {
  border-style: dotted solid double dashed;
}

/* 3개 값 */
p {
  border-style: dotted solid double;
}

/* 2개 값 */
p {
  border-style: dotted solid;
}

/* 1개 값 */
p {
  border-style: dotted;
}
```

## border - 축약 속성

테두리를 다룰 때 고려해야 할 특성이 많이 있습니다.

코드를 단축하기 위해 하나의 속성에서 모든 개별 테두리 속성을 지정할 수도 있습니다.

```border``` 속성은 다음과 같은 개별 테두리 속성에 대한 축약 속성입니다.

+ ```border-width```
+ ```border-style``` (필수)
+ ```border-color```

###### 예제 12

```css
p {
  border: 5px solid red;
}
```

결과 : 

<p style="border: 5px solid red;">축약 테두리 속성</p>

한 변에 대해서만 모든 개별 테두리 속성을 지정할 수도 있습니다.

###### 예제 13

```css
p {
  border-left: 6px solid red;
}
```

결과 : 

<p style="border-left: 6px solid red;">축약 테두리 속성</p>

###### 예제 14

```css
p {
  border-bottom: 6px solid red;
}
```

결과 : 

<p style="border-bottom: 6px solid red;">축약 테두리 속성</p>

## border-radius

```border-radius``` 속성은 둥근 모서리를 요소에 추가하는 데 사용됩니다.

###### 예제 15

```css
p {
  border: 2px solid red;
  border-radius: 5px;
}
```

결과 : 

<p style="border: 2px solid red; border-radius: 5px;">둥근 </p>
