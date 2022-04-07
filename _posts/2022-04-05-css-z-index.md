---
layout: post
title: CSS 23. z-index
subtitle: z-index 속성은 요소의 스택 순서를 지정합니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS z-index

## z-index 속성

요소가 배치되면 다른 요소와 겹칠 수 있습니다.

```z-index``` 속성은 요소의 스택 순서(다른 요소의 앞이나 뒤에 배치할 요소)를 지정합니다.

요소의 스택 순서는 양수 또는 음수일 수 있습니다.

###### 예제 1

```css
img {
  position: absolute;
  left: 0px;
  top: 0px;
  z-index: -1;
}
```

## 다른 z-index 예제

```html
<html>
<head>
<style>
.container {
  position: relative;
}

.black-box {
  position: relative;
  z-index: 1;
  border: 2px solid black;
  height: 100px;
  margin: 30px;
}

.gray-box {
  position: absolute;
  z-index: 3;
  background: lightgray;
  height: 60px;
  width: 70%;
  left: 50px;
  top: 50px;
}

.green-box {
  position: absolute;
  z-index: 2;
  background: lightgreen;
  width: 35%;
  left: 270px;
  top: -15px;
  height: 100px;
}
</style>
</head>
<body>

<div class="container">
  <div class="black-box">Black box</div>
  <div class="gray-box">Gray box</div>
  <div class="green-box">Green box</div>
</div>

</body>
</html>
```

## z-index 미포함

```z-index```를 지정하지 않고 두 개의 위치 요소가 서로 겹치는 경우 HTML 코드에서 마지막으로 정의된 요소가 맨 위에 표시됩니다.

###### 예제 2

```html
<html>
<head>
<style>
.container {
  position: relative;
}

.black-box {
  position: relative;
  border: 2px solid black;
  height: 100px;
  margin: 30px;
}

.gray-box {
  position: absolute;
  background: lightgray;
  height: 60px;
  width: 70%;
  left: 50px;
  top: 50px;
}

.green-box {
  position: absolute;
  background: lightgreen;
  width: 35%;
  left: 270px;
  top: -15px;
  height: 100px;
}
</style>
</head>
<body>

<div class="container">
  <div class="black-box">Black box</div>
  <div class="gray-box">Gray box</div>
  <div class="green-box">Green box</div>
</div>

</body>
</html>
```
