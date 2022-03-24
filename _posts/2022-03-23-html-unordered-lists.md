---
layout: post
title: HTML 16-1. 순서 없는 리스트 (Unordered Lists)
subtitle: HTML ul 태그는 순서가 매겨지지 않은(블렛이 붙은) 목록을 정의합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 순서 없는(Unordered) 리스트

## HTML 순서 없는(Unordered) 리스트

순서 없는 리스트는 ```<ul>``` 태그로 시작합니다. 각 목록 항목은 ```<li>``` 태그로 시작합니다.

목록 항목은 기본적으로 글머리 기호(작은 검은색 원)로 표시됩니다.

###### 예제 1

```html
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

## HTML 순서 없는 리스트 - 리스트 마커 선택

CSS ```list-style-type``` 속성은 목록 항목 마커의 스타일을 정의하는 데 사용됩니다. 다음의 몇개의 값을 지정할 수 있습니다.

| 값 | 설명 |
| disc | 리스트 항목 마커를 글머리 기호로 설정합니다(기본값). |
| circle | 리스트 항목 마커를 원으로 설정합니다. |
| square | 리스트 항목 마커를 정사각형으로 설정합니다. |
| none | 리스트 항목이 표시되지 않습니다. |

###### 예제 2 - disc

```html
<ul style="list-style-type:disc;">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

###### 예제 2 - circle

```html
<ul style="list-style-type:circle;">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

###### 예제 2 - square

```html
<ul style="list-style-type:square;">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

###### 예제 2 - none

```html
<ul style="list-style-type:none;">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

## 중첩 HTML 리스트

목록을 중첩할 수 있습니다.(목록 내부)

###### 예제 3

```html
<ul>
  <li>Coffee</li>
  <li>Tea
    <ul>
      <li>Black tea</li>
      <li>Green tea</li>
    </ul>
  </li>
  <li>Milk</li>
</ul>
```

{: .box-note}
**Note:** 리스트 항목(```<li>```)에는, 새로운 리스트와 그 외의 HTML 요소(이미지나 링크등)를 포함할 수 있습니다.

## CSS를 사용한 수평 리스트

HTML 리스트는 CSS를 사용하여 다양한 방법으로 스타일링할 수 있습니다.

일반적인 방법 중 하나는 목록을 가로로 스타일링하여 탐색 메뉴를 만드는 것입니다.

###### 예제 4

```html
<!DOCTYPE html>
<html>
<head>
<style>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333333;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #111111;
}
</style>
</head>
<body>

<ul>
  <li><a href="#home">Home</a></li>
  <li><a href="#news">News</a></li>
  <li><a href="#contact">Contact</a></li>
  <li><a href="#about">About</a></li>
</ul>

</body>
</html>
```

## Summary

+ HTML ```<ul>``` 요소를 사용하여 순서 없는 목록을 정의합니다.
+ CSS ```list-style-type``` 속성을 사용하여 목록 항목 마커를 정의합니다.
+ HTML ```<li>``` 요소를 사용하여 목록 항목을 정의합니다.
+ 리스트는 중첩 할 수 있습니다.
+ 목록 항목은 다른 HTML 요소를 포함할 수 있습니다.
+ 목록을 가로로 표시하려면 CSS 속성 ```float: left``` 를 사용합니다.
