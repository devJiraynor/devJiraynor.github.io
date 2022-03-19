---
layout: post
title: HTML 6.스타일(Style)
subtitle: HTML 스타일 속성은 색상, 글꼴, 크기 등의 스타일을 요소에 추가하는 데 사용됩니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 스타일

## HTML Style 속성

HTML 요소의 스타일 설정은 ```style``` 속성을 사용하여 수행할 수 있습니다.

HTML ```style``` 속성 구문은 다음과 같습니다.

```html
<tagname style="property:value;">
```

**property**는 CSS 속성입니다. *value*는 CSS 값입니다.

## 배경 색

CSS ```background-color``` 속성은 HTML 요소의 배경색을 정의합니다.

###### 예제 1 (페이지 전체 색상)

```html
<body style="background-color:powderblue;">

<h1>표제입니다.</h1>
<p>단락입니다.</p>

</body>
```

###### 예제 2 (각 태그마다 색상)

```html
<body>

<h1 style="background-color:powderblue;">표제입니다.</h1>
<p style="background-color:tomato;">단락입니다.</p>

</body>
```

## 텍스트 색상

CSS ```color``` 속성은 HTML 요소의 텍스트 색상을 정의합니다.

###### 예제 3

```html
<h1 style="color:blue;">표제입니다.</h1>
<p style="color:red;">단락입니다.</p>
```

## 글꼴

CSS ```font-family``` 속성은 HTML 요소에 사용할 글꼴을 정의합니다.

###### 예제 4

```html
<h1 style="font-family:verdana;">표제입니다</h1>
<p style="font-family:courier;">단락입니다.</p>
```

## 텍스트 크기

CSS ```font-size``` 속성은 HTML 요소의 텍스트 크기를 정의합니다.

###### 예제 5

```html
<h1 style="font-size:300%;">표제입니다.</h1>
<p style="font-size:160%;">단락입니다.</p>
```

## 텍스트 정렬

CSS ```text-align``` 속성은 HTML 요소의 수평 텍스트 정렬을 정의합니다.

###### 예제 6

```html
<h1 style="text-align:center;">표제입니다.</h1>
<p style="text-align:center;">단락입니다..</p>
```

## Summary

+HTML 요소의 스타일 지정에 ```style``` 속성 사용
+배경색으로 ```background-color``` 사용
+텍스트 색상에 ```color``` 사용
+텍스트 글꼴에 ```font-family``` 사용
+텍스트 크기에 ```font-size``` 사용
+텍스트 정렬에 ```text-align``` 사용
