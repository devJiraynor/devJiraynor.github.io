---
layout: post
title: CSS 32. 네비게이션 바 (Navigation Bar)
subtitle: CSS를 사용하면 지루한 HTML 메뉴를 보기 좋은 네비게이션으로 변환할 수 있습니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 네비게이션 바

모든 웹 사이트에서 사용하기 쉬운 네비게이션을 사용하는 것이 중요합니다.

CSS를 사용하면 지루한 HTML 메뉴를 보기 좋은 네비게이션 바로 변환할 수 있습니다.

## 네비게이션 바 = 링크들의 링크

네비게이션 바에는 표준 HTML이 기본으로 필요합니다.

이 예에서는 표준 HTML 목록에서 네비게이션 바를 만들 것입니다.

네비게이션 바은 기본적으로 링크 목록이기 때문에, ```<ul>``` 및 ```<li>``` 요소를 사용합니다.

###### 예제 1

```html
<ul>
  <li><a href="default.asp">Home</a></li>
  <li><a href="news.asp">News</a></li>
  <li><a href="contact.asp">Contact</a></li>
  <li><a href="about.asp">About</a></li>
</ul>
```

이제 글머리 기호와 여백, 패딩을 목록에서 제거해 보겠습니다.

###### 예제 2

```css
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
```

예제 설명 :

+ ```list-style-type: none;``` - 글머리 기호를 제거합니다. 네비게이션 바에는 목록 마커가 필요하지 않습니다.
+ ```margin: 0;```으로 설정하고 ```padding: 0;```으로 설정하여 브라우저 기본 설정을 제거합니다.

## 수직 네비게이션 바

수직 탐색 막대를 작성하려면 이전 코드와 함께 목록 내부의 ```<a>``` 요소를 스타일링합니다.

###### 예제 3

```css
li a {
  display: block;
  width: 60px;
}
```

예제 설명 :

+ ```display: block;``` - 링크를 블록 요소로 표시하면 텍스트뿐만 아니라 전체 링크 영역을 클릭할 수 있으며, 원하는 경우 너비, 여백, 높이 등을 지정할 수 있습니다.
+ ```width: 60px;``` - 블록 요소는 기본적으로 사용 가능한 전체 너비를 차지합니다. 60픽셀 너비를 지정합니다.

또한 블록 요소로 표시될 때 사용 가능한 전체 너비를 차지하므로 너비를 ```<ul>```로 설정하고 너비를 제거할 수 있습니다. 그러면 이전 예제와 동일한 결과가 나타납니다.

###### 예제 4

```css
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 60px;
}

li a {
  display: block;
}
```

## 수직 네비게이션 바 예제

회색 배경색으로 기본 수직 탐색 모음을 만들고 사용자가 마우스를 링크 위로 이동할 때 링크의 배경색을 변경합니다.

###### 예제 5

```css
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 200px;
  background-color: #f1f1f1;
}

li a {
  display: block;
  color: #000;
  padding: 8px 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #555;
  color: white;
}
```

#### active 네비게이션 링크

현재 링크에 "active" 클래스를 추가하여 사용자가 어떤 페이지에 있는지 알 수 있습니다.

###### 예제 6

```css
.active {
  background-color: #04AA6D;
  color: white;
}
```

#### 가운데 정렬 및 테두리 추가

```text-align:center```를 ```<li>``` 또는 ```<a>```에 추가하여 링크를 중앙에 배치합니다.

```border``` 속성으로 ```<ul>``` 네비게이션 바 주위에 경계선을 추가합니다. 또한 네비게이션 바 내부에 테두리를 두려면 마지막 요소를 제외한 모든 ```<li>``` 요소에 테두리 하단을 추가합니다.

###### 예제 7

```css
ul {
  border: 1px solid #555;
}

li {
  text-align: center;
  border-bottom: 1px solid #555;
}

li:last-child {
  border-bottom: none;
}
```

## 전체 높이 고정 수직 네비게이션 바

전체 높이 고정 수직 네비게이션 바를 만듭니다.

###### 예제 8

```css
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 25%;
  background-color: #f1f1f1;
  height: 100%; /* 전체 높이 */
  position: fixed; /* 스크롤 되더라도 고정되도록 함 */
  overflow: auto; /* 네비게이션 목록 많아지면 스크롤 되도록 함 */
}
```

## 수평 네비게이션 바

수평 네비게이션 바를 만드는 **inline** 또는 **float** 리스트 사용이라는 두 가지 방법이 있습니다. 

#### Inline List Items

수평 네비게이션 바를 만드는 한 가지 방법은 "표준" 코드 외에 ```<li>``` 요소를 인라인으로 지정하는 것입니다.

###### 예제 9

```css
li {
  display: inline;
}
```

예제 설명 :

+ ```display: inline;``` - 기본적으로 ```<li>``` 요소는 블록 요소입니다. 여기서는 각 목록 항목 앞뒤의 줄 바꿈을 제거하여 한 줄에 표시합니다.

#### Floating List Items

수평 네비게이션 바를 만드는 또 다른 방법은 ```<li>``` 요소를 플로팅하고 네비게이션 링크의 레이아웃을 지정하는 것입니다.

###### 예제 10

```css
li {
  float: left;
}

a {
  display: block;
  padding: 8px;
  background-color: #dddddd;
}
```

예제 설명 :

+ ```float: left;``` - ```float```을 사용하여 블록 요소가 서로 나란히 플로팅되도록 합니다.
+ ```display: block;``` - 패딩을 지정할 수 있습니다(필요한 경우 높이, 폭, 여백 등).
+ ```padding: 8px;``` - 각 ```<a>``` 요소 사이에 일부 패딩을 지정하여 보기 좋게 만듭니다.
+ ```background-color: #dddddd;``` - 각 ```<a>``` 요소에 회색 배경 색상을 추가합니다.

**Tip:** 전체 너비의 배경색을 원하는 경우 각 ```<a>``` 요소 대신 배경색을 ```<ul>```에 추가합니다.

###### 예제 11

```css
ul {
  background-color: #dddddd;
}
```

## 수평 네비게이션 바 예제

어두운 배경색으로 기본 수평 탐색 모음을 만들고 사용자가 마우스를 링크 위로 이동할 때 링크의 배경색을 변경합니다.

###### 예제 12

```css
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #111;
}
```

#### active 네비게이션 링크

현재 링크에 "active" 클래스를 추가하여 사용자가 어떤 페이지에 있는지 알 수 있습니다.

###### 예제 13

```css
.active {
  background-color: #04AA6D;
}
```

#### 오른쪽 정렬 링크

리스트 항목을 오른쪽으로 이동하여 링크를 오른쪽 정렬합니다(```float:right;```).

###### 예제 14

```html
<ul>
  <li><a href="#home">Home</a></li>
  <li><a href="#news">News</a></li>
  <li><a href="#contact">Contact</a></li>
  <li style="float:right"><a class="active" href="#about">About</a></li>
</ul>
```

#### 구분 테두리

```border-right``` 속성을 ```<li>```에 추가하여 링크 구분선을 만듭니다.

###### 예제 15

```css
li {
  border-right: 1px solid #bbb;
}

li:last-child {
  border-right: none;
}
```

#### 고정 네비게이션 바

사용자가 페이지를 스크롤할 때에도 네비게이션 바를 페이지의 맨 위 또는 맨 아래에 고정할 수 있습니다.

###### 예제 16 - 상단 고정

```css
ul {
  position: fixed;
  top: 0;
  width: 100%;
}
```

###### 예제 17 - 하단 고정

```css
ul {
  position: fixed;
  bottom: 0;
  width: 100%;
}
```

{: .box-note}
**Note:** 모바일 장치에서 고정 위치가 제대로 작동하지 않을 수 있습니다.

#### 회색 수평 네비게이션 바

회색 테두리와 얇은 회색 바탕의 수평 네비게이션 바의 예

###### 예제 18

```css
ul {
  border: 1px solid #e7e7e7;
  background-color: #f3f3f3;
}

li a {
  color: #666;
}
```

#### sticky 네비게이션 바

고정 네비게이션 바를 만들려면 ```position: sticky;```을 ```<ul>```에 추가합니다.

```sticky``` 요소는 스크롤 위치에 따라 상대 요소와 고정 요소를 전환합니다. 뷰포트에서 지정된 오프셋 위치가 충족될 때까지 상대적인 위치에 배치됩니다. 그런 다음 한자리에 고정됩니다.

###### 예제 19

```css
ul {
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
}
```

{: .box-note}
**Note:** Internet Explorer는 고정 위치를 지원하지 않습니다. Safari에는 ```-webkit-``` 접두사가 필요합니다. 또한 고정 위치가 작동하려면 상단, 오른쪽, 하단 또는 왼쪽 중 하나 이상을 지정해야 합니다.
