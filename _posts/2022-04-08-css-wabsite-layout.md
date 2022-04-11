---
layout: post
title: CSS 39. 웹사이트 레이아웃 (Website Layout)
subtitle: 웹 사이트는 머리글, 메뉴, 내용 및 바닥글로 나뉩니다. 선택할 수 있는 다양한 레이아웃 디자인이 많이 있습니다. 그러나 이 구조는 가장 일반적인 구조 중 하나입니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 웹 사이트 레이아웃

## 헤더 (Header)

헤더는 일반적으로 웹 사이트의 맨 위(또는 탐색 메뉴 바로 아래)에 있습니다. 로고 또는 웹 사이트 이름이 포함되어 있는 경우가 많습니다.

###### 예제 1

```css
.header {
  background-color: #F1F1F1;
  text-align: center;
  padding: 20px;
}
```

## 네비게이션 바 (Navigation Bar)

네비게이션 바에는 웹 사이트를 탐색하는 방문자에게 도움이 되는 링크 목록이 포함되어 있습니다.

###### 예제 2

```css
/* 네비게이션 바 컨테이너 */
.topnav {
  overflow: hidden;
  background-color: #333;
}

/* 네비게이션 바 링크 */
.topnav a {
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

/* 링크 호버 */
.topnav a:hover {
  background-color: #ddd;
  color: black;
}
```

## 컨텐츠 (Content)

이 섹션의 레이아웃은 대상 사용자에 따라 달라지는 경우가 많습니다. 가장 일반적인 레이아웃은 다음 중 하나(또는 이들을 조합)입니다.

+ **1-column** (모바일 브라우저에 자주 사용됨)
+ **2-column** (태블릿과 노트북에 자주 사용됨)
+ **3-column layout** (데스크톱에만 사용됨)

3-column 레이아웃을 만들고 더 작은 화면에서 1-column 레이아웃으로 변경합니다.

###### 예제 3

```css
/* 세 개의 동일한 컬럼 만들기 */
.column {
  float: left;
  width: 33.33%;
}

/* 컬럼 뒤의 float clear */
.row:after {
  content: "";
  display: table;
  clear: both;
}

/* 반응형 레이아웃 - 작은 화면에서 세 개의 컬럼이 서로 나란히 쌓이지 않도록 합니다(600px 너비 이하). */
@media screen and (max-width: 600px) {
  .column {
    width: 100%;
  }
}
```

## 동일하지 않은 컬럼 (Unequal Columns)

주요 컨텐츠는 당신의 사이트에서 가장 크고 중요한 부분입니다.

열 너비가 **동일하지 않은 것**이 일반적이어서 대부분의 공간이 주 콘텐츠용으로 예약되어 있습니다. 사이드 컨텐츠(있는 경우)는 종종 대체 탐색 또는 주요 컨텐츠와 관련된 정보를 지정하는 데 사용됩니다. 원하는 대로 너비를 변경하십시오. 총 합계는 최대 100%여야 합니다.

###### 예제 4

```css
.column {
  float: left;
}

/* 사이드 컬럼 */
.column.side {
  width: 25%;
}

/* 중간 크기 컬럼 */
.column.middle {
  width: 50%;
}

/*  반응형 레이아웃 - 작은 화면에서 모든 이 서로 나란히 쌓이지 않도록 합니다(600px 너비 이하). */
@media screen and (max-width: 600px) {
  .column.side, .column.middle {
    width: 100%;
  }
}
```

## 바닥글 (Footer)

바닥글은 페이지 하단에 있습니다. 여기에는 저작권 및 연락처 정보와 같은 정보가 포함되어 있는 경우가 많습니다.

###### 예제 5

```css
.footer {
  background-color: #F1F1F1;
  text-align: center;
  padding: 10px;
}
```

## 반응형 웹사이트 레이아웃

위의 CSS 코드 중 일부를 사용하여 화면 너비에 따라 두 열과 전체 너비 열 사이에서 변화하는 대응 웹 사이트 레이아웃을 만들었습니다.

###### 예제 6

```html
<!DOCTYPE html>
<html>
<head>
<style>
* {
  box-sizing: border-box;
}

body {
  font-family: Arial;
  padding: 10px;
  background: #f1f1f1;
}

.header {
  padding: 30px;
  text-align: center;
  background: white;
}

.header h1 {
  font-size: 50px;
}

.topnav {
  overflow: hidden;
  background-color: #333;
}

.topnav a {
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

.topnav a:hover {
  background-color: #ddd;
  color: black;
}

.leftcolumn {   
  float: left;
  width: 75%;
}

.rightcolumn {
  float: left;
  width: 25%;
  background-color: #f1f1f1;
  padding-left: 20px;
}

.fakeimg {
  background-color: #aaa;
  width: 100%;
  padding: 20px;
}

.card {
  background-color: white;
  padding: 20px;
  margin-top: 20px;
}

.row:after {
  content: "";
  display: table;
  clear: both;
}

.footer {
  padding: 20px;
  text-align: center;
  background: #ddd;
  margin-top: 20px;
}

@media screen and (max-width: 800px) {
  .leftcolumn, .rightcolumn {   
    width: 100%;
    padding: 0;
  }
}

@media screen and (max-width: 400px) {
  .topnav a {
    float: none;
    width: 100%;
  }
}
</style>
</head>
<body>

<div class="header">
  <h1>My Website</h1>
  <p>Resize the browser window to see the effect.</p>
</div>

<div class="topnav">
  <a href="#">Link</a>
  <a href="#">Link</a>
  <a href="#">Link</a>
  <a href="#" style="float:right">Link</a>
</div>

<div class="row">
  <div class="leftcolumn">
    <div class="card">
      <h2>TITLE HEADING</h2>
      <h5>Title description, Dec 7, 2017</h5>
      <div class="fakeimg" style="height:200px;">Image</div>
      <p>Some text..</p>
      <p>Sunt in culpa qui officia deserunt mollit anim id est laborum consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.</p>
    </div>
    <div class="card">
      <h2>TITLE HEADING</h2>
      <h5>Title description, Sep 2, 2017</h5>
      <div class="fakeimg" style="height:200px;">Image</div>
      <p>Some text..</p>
      <p>Sunt in culpa qui officia deserunt mollit anim id est laborum consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.</p>
    </div>
  </div>
  <div class="rightcolumn">
    <div class="card">
      <h2>About Me</h2>
      <div class="fakeimg" style="height:100px;">Image</div>
      <p>Some text about me in culpa qui officia deserunt mollit anim..</p>
    </div>
    <div class="card">
      <h3>Popular Post</h3>
      <div class="fakeimg"><p>Image</p></div>
      <div class="fakeimg"><p>Image</p></div>
      <div class="fakeimg"><p>Image</p></div>
    </div>
    <div class="card">
      <h3>Follow Me</h3>
      <p>Some text..</p>
    </div>
  </div>
</div>

<div class="footer">
  <h2>Footer</h2>
</div>

</body>
</html>
```
