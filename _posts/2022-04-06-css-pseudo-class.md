---
layout: post
title: CSS 29. 유사 클래스 (Pseudo-classes)
subtitle: CSS 유사 클래스에 대해 알아봅니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 유사 클래스

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
