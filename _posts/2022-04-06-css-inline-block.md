---
layout: post
title: CSS 26. Inline-Block
subtitle: display: inline과 비교했을 때, display: inline-block은 요소의 너비와 높이를 설정할 수 있다는 점이 가장 큰 차이점입니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 레이아웃 - display: inline-block

## display: inline-block 값

```display: inline;```과 비교했을 때, ```display: inline-block;```은 요소의 너비와 높이를 설정할 수 있다는 점이 가장 큰 차이점입니다.

또한 ```display: inline-block;```의 경우 상단 및 하단 여백/패딩을 존중하지만 ```display: inline;```은 그렇지 않습니다.

```display: block;```과 비교하여 가장 큰 차이점은 ```display: inline-block```은 요소 뒤에 줄 바꿈을 추가하지 않으므로 요소가 다른 요소 옆에 앉을 수 있다는 것입니다.

다음 예제에서는 ```display: inline;```, ```display: inline-block```, ```display: block```의 다양한 동작을 보여 줍니다.

###### 예제 1

```css
span.a {
  display: inline; /* the default for span */
  width: 100px;
  height: 100px;
  padding: 5px;
  border: 1px solid blue;
  background-color: yellow;
}

span.b {
  display: inline-block;
  width: 100px;
  height: 100px;
  padding: 5px;
  border: 1px solid blue;
  background-color: yellow;
}

span.c {
  display: block;
  width: 100px;
  height: 100px;
  padding: 5px;
  border: 1px solid blue;
  background-color: yellow;
}
```

## 인라인 블록을 사용하여 탐색 링크 작성

표시에 일반적으로 사용되는 한 가지 방법은 ```display: inline-block;```은 목록 항목을 수직이 아닌 수평으로 표시하는 것입니다. 다음 예제에서는 수평 탐색 링크를 만듭니다.

###### 예제 2

```css
.nav {
  background-color: yellow;
  list-style-type: none;
  text-align: center; 
  padding: 0;
  margin: 0;
}

.nav li {
  display: inline-block;
  font-size: 20px;
  padding: 20px;
}
```
