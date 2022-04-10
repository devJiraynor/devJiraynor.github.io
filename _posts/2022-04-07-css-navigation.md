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

