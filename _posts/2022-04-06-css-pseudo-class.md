---
layout: post
title: CSS 29. 유사 클래스 (Pseudo-classes)
subtitle: CSS 유사 클래스에 대해 알아봅니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 유사 클래스 (Pseudo-classes)

## 유사 클래스란?

유사 클래스는 요소의 특수 상태를 정의하는 데 사용됩니다.

예를 들어 다음과 같은 용도로 사용할 수 있습니다.

+ 사용자가 요소 위로 마우스를 가져가면 요소 스타일 지정
+ 방문한 링크와 방문하지 않은 링크의 스타일 지정
+ 요소가 포커스가 되면 스타일 지정

## 구문

유사 클래스의 구문:

```css
selector:pseudo-class {
  property: value;
}
```

## 앵커 유사 클래스

링크는 다음과 같은 다양한 방법으로 표시할 수 있습니다.

###### 예제 1

```css
/* 방문하지 않은 링크 */
a:link {
  color: #FF0000;
}

/* 방문 링크 */
a:visited {
  color: #00FF00;
}

/* 마우스 오버 링크 */
a:hover {
  color: #FF00FF;
}

/* 선택된 링크 */
a:active {
  color: #0000FF;
}
```

{: .box-note}
**Note:** ```a:hover```를 사용하려면 CSS 정의에서 ```a:link```와 ```a:visited``` 뒤에 와야 합니다! ```a:active```를 사용하려면 CSS 정의에서 ```a:hover``` 뒤에 와야 합니다! 유사 클래스 이름은 대소문자를 구분하지 않습니다.

## 유사 클래스와 HTML 클래스

유사 클래스는 HTML 클래스와 결합할 수 있습니다.

예제에서 링크 위에 마우스를 놓으면 색상이 바뀝니다.

###### 예제 2

```css
a.highlight:hover {
  color: #ff0000;
}
```

## ```<div>``` 호버 (hover)

```<div>``` 요소에 ```:hover``` 유사 클래스를 사용하는 예:

###### 예제 3

```css
div:hover {
  background-color: blue;
}
```

## 심플 툴팁 호버 (hover)

```<div>``` 요소 위에 마우스를 놓으면 (툴 팁과 같이) ```<p>``` 요소가 표시됩니다.

###### 예제 4

```css
p {
  display: none;
  background-color: yellow;
  padding: 20px;
}

div:hover p {
  display: block;
}
```

## ```:first-child``` 유사 클래스

```:first-child``` 유사 클래스는 다른 요소의 첫 번째 자식인 지정된 요소와 일치합니다.

#### 첫 번째 ```<p>``` 요소와 일치

다음 예제에서는 셀렉터가 요소의 첫 번째 자식인 모든 ```<p>``` 요소와 일치합니다.

###### 예제 5

```css
p:first-child {
  color: blue;
}
```

#### 모든 ```<p>``` 요소의 첫 번째 ```<i>``` 요소를 일치

다음 예제에서는 셀렉터가 모든 ```<p>``` 요소의 첫 번째 ```<i>``` 요소와 일치합니다.

###### 예제 6

```css
p i:first-child {
  color: blue;
}
```

## 모든 첫 번째 자식 ```<p>``` 요소의 모든 ```<i>``` 요소 일치

다음 예제에서는 셀렉터가 다른 요소의 첫 번째 자식인 ```<p>``` 요소의 모든 ```<i>``` 요소와 일치합니다.

###### 예제 7

```css
p:first-child i {
  color: blue;
}
```

## ```:lang``` 유사 클래스

```:lang``` 유사 클래스를 사용하면 다른 언어에 대한 특수 규칙을 정의할 수 있습니다.

아래 예에서 ```lang```은 lang="no"로 ```<q>``` 요소에 대한 따옴표를 정의합니다.

###### 예제 8

```html
<html>
<head>
<style>
q:lang(no) {
  quotes: "~" "~";
}
</style>
</head>
<body>

<p>Some text <q lang="no">A quote in a paragraph</q> Some text.</p>

</body>
</html>
```

