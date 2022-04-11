---
layout: post
title: CSS 41. 특이도 (Specificity) - 우선순위
subtitle: 동일한 요소를 가리키는 CSS 규칙이 두 개 이상일 경우 처리 결과에 대해 알아봅니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 특이도 (Specificity)

## 특이도란?

동일한 요소를 가리키는 CSS 규칙이 두 개 이상일 경우, 가장 높은 특이도 값을 가진 셀렉터가 "우승"하며, 스타일 선언이 해당 HTML 요소에 적용될 것입니다.

특수성을 요소에 최종적으로 적용할 스타일 선언을 결정하는 점수/순위로 간주합니다.

###### 예제 1 - "p" 요소를 셀렉터로 사용하고 이 요소에 대한 빨간색 색상을 지정했습니다. 텍스트는 빨간색으로 표시됩니다.

```html
<html>
<head>
  <style>
    p {color: red;}
  </style>
</head>
<body>

<p>Hello World!</p>

</body>
</html>
```

###### 예제 2 - 클래스 셀렉터("test")를 추가하고 이 클래스에 대해 녹색을 지정했습니다. 요소 셀렉터 "p"에 빨간색 색상을 지정했음에도 불구하고 텍스트가 녹색이 됩니다. 이는 클래스 선택기에 더 높은 우선 순위가 부여되기 때문입니다.

```html
<html>
<head>
  <style>
    .test {color: green;}
    p {color: red;}
  </style>
</head>
<body>

<p class="test">Hello World!</p>

</body>
</html>
```

###### 예제 3 - id 셀렉터("demo")를 추가했습니다. id 선택기에 더 높은 우선 순위가 부여되기 때문에 텍스트는 이제 파란색이 됩니다.

```html
<html>
<head>
  <style>
    #demo {color: blue;}
    .test {color: green;}
    p {color: red;}
  </style>
</head>
<body>

<p id="demo" class="test">Hello World!</p>

</body>
</html>
```

###### 예제 4 - "p" 요소에 대한 인라인 스타일을 추가했습니다. 인라인 스타일에 가장 높은 우선 순위가 부여되므로 텍스트는 이제 분홍색이 됩니다.

```html
<html>
<head>
  <style>
    #demo {color: blue;}
    .test {color: green;}
    p {color: red;}
  </style>
</head>
<body>

<p id="demo" class="test" style="color: pink;">Hello World!</p>

</body>
</html>
```

## 특이도 계층구조

모든 CSS 셀렉터는 특이도 계층에서 자신의 위치를 갖습니다.

셀렉터의 특이도 수준을 정의하는 네 가지 범주가 있습니다.

+ **Inline styles** - 예: ```<h1 style="color: pink;">```
+ **IDs** - 예: ```#navbar```
+ **Classes, pseudo-classes, attribute selectors** - 예: ```.test```, ```:hover```, ```[href]```
+ **Elements, pseudo-elements** - 예: ```h1```, ```:before```

## 특이도 계산 방법

특이성을 계산하는 방법을 기억하세요

0에서 시작하여 각 ID 값에 100을 추가하고, 각 클래스 값(또는 유사 클래스 또는 속성 선택기)에 10을 추가하고, 각 요소 선택기 또는 유사 요소에 1을 추가합니다.

{: .box-note}
**Note:** 인라인 스타일은 1000의 특이도 값을 가지며 항상 가장 높은 우선 순위가 부여됩니다!<br>**Note:** 이 규칙에는 예외가 하나 있습니다. ```!important``` 규칙을 사용하면 인라인 스타일도 재정의됩니다!

아래 표에는 특이도 값을 계산하는 방법에 대한 몇 가지 예가 나와 있습니다.

| **셀렉터** | **특이도 값** | **계산** |
| ```p``` | 1 | 1 |
| ```p.text``` | 11 | 1 + 10 |
| ```p#demo``` | 101 | 1 + 100  |
| ```<p style="color: pink;">``` | 1000 | 1000 |
| ```#demo``` | 100 | 100 |
| ```.test``` | 10 | 10 |
| ```p.test1.test2``` | 21 | 1 + 10 + 10 |
| ```#navbar p#demo``` | 201 | 100 + 1 + 100 |
| * | 0 | 0 |

특이도 값이 가장 높은 셀렉터가 승리하여 적용됩니다!

다음 세 가지 코드의 특이도를 계산해보세요.

###### 예제 5

```html
A: h1
B: h1#content
C: <h1 id="content" style="color: pink;">Heading</h1>
```

A의 특이도는 1(원소 선택기 1개)입니다.
B의 특이도는 101(ID 기준 1개 + 요소 선택기 1개)입니다.
C의 특이도는 1000(인라인 스타일링)입니다.

세 번째 규칙(C)의 특이도 값이 가장 높기 때문에(1000) 이 스타일 선언이 적용됩니다.

## 특이도 규칙 추가 예제

**특이도가 같을 때는 나중에 온 규칙이 승리**

###### 예제 6

```css
h1 {background-color: yellow;}
h1 {background-color: red;}
```

**ID 셀렉터가 속성 셀렉터보다 더 높은 특이도을 가짐**

###### 예제 7

```css
div#a {background-color: green;}
#a {background-color: yellow;}
div[id=a] {background-color: blue;}
```

**내부 스타일 셀렉터는 외부 스타일 셀렉터보다 더 높은 우선순위를 가짐**

###### 예제 8

```html
From external CSS file:
#content h1 {background-color: red;}

In HTML file:
<style>
#content h1 {background-color: yellow;}
</style>
```

**클래스 셀렉터가 요소 셀렉터보다 높은 특이도를 가짐**

###### 예제 9

```css
.intro {background-color: yellow;}
h1 {background-color: red;}
```

**범용 선택기(```*```) 및 상속된 값의 특수성은 0입니다.**

