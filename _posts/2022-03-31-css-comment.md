---
layout: post
title: CSS 05. 주석 (Comments)
subtitle: CSS 주석은 브라우저에 표시되지 않지만 소스 코드를 문서화하는 데 도움이 됩니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 주석

## CSS 주석

주석은 코드를 설명하는 데 사용되며 나중에 소스 코드를 편집할 때 도움이 될 수 있습니다.

브라우저에서는 주석이 무시됩니다.

CSS 주석은 ```<style>``` 요소 내부에 배치되어 ```/*``` 로 시작하여 ```*/``` 로 끝납니다.

###### 예제 1

```css
/* 이것은 한 줄 주석입니다. */
p {
  color: red;
}
```

코드의 임의의 장소에 코멘트를 추가할 수 있습니다.

###### 예제 2

```css
p {
  color: red;  /* 텍스트 색상을 빨간색으로 설정 */
}
```

주석은 복수의 행에 걸칠 수도 있습니다.

###### 예제 3

```css
/* 이것은
복수행 
주석입니다. */

p {
  color: red;
}
```

## HTML 및 CSS 주석

HTML 의 주석은 ```<!-- ... -->```구문입니다.

다음 예에서는 HTML 주석과 CSS 주석을 사용하고 있습니다.

###### 예제 4

```html
<!DOCTYPE html>
<html>
<head>
<style>
p {
  color: red; /* 텍스트 색상을 빨간색으로 설정 */
}
</style>
</head>
<body>

<h2>My Heading</h2>

<!-- 이 문단들은 붉은 글씨로 표기됩니다. -->
<p>Hello World!</p>
<p>This paragraph is styled with CSS.</p>
<p>CSS comments are not shown in the output.</p>

</body>
</html>
```
