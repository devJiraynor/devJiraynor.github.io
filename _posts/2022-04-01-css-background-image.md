---
layout: post
title: CSS 07-1. 배경 이미지 (Background Image)
subtitle: background-image 속성은 요소의 배경으로 사용할 이미지를 지정합니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 배경 이미지

## background-image

```background-image``` 속성은 요소의 배경으로 사용할 이미지를 지정합니다.

기본적으로는 이미지가 반복되어 전체 요소를 커버합니다.

###### 예제 1

```css
body {
  background-image: url("paper.gif");
}
```

{: .box-note}
**Note:** 배경 이미지를 사용할 때는 텍스트를 방해하지 않는 이미지를 사용하십시오.

```<p>``` 요소와 같은 특정 요소에 대해 배경 이미지를 설정할 수도 있습니다.

```css
p {
  background-image: url("paper.gif");
}
```
