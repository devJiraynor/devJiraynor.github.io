---
layout: post
title: CSS 07-2. 배경 이미지 반복 (Background Image Repeat)
subtitle: 기본적으로 background-image 속성은 이미지를 수평 및 수직 모두 반복합니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 배경 이미지 반복

## background-repeat

기본적으로 ```background-image``` 속성은 이미지를 수평 및 수직 모두 반복합니다.

일부 이미지는 수평 또는 수직으로만 반복해야 합니다. 그렇지 않으면 다음과 같이 이상하게 표시됩니다.

###### 예제 1

```css
body {
  background-image: url("gradient_bg.png");
}
```

위 이미지가 수평으로만 반복되면(```background-repeat: repeat-x;```), 배경이 더 좋아집니다.

###### 예제 2

```css
body {
  background-image: url("gradient_bg.png");
  background-repeat: repeat-x;
}
```

{: .box-note}
**Tip:** 이미지를 수직으로 반복하려면 ```background-repeat: repeat-y;```를 설정합니다.

## background-repeat: no-repeat

배경 이미지를 한 번만 표시하는 것도 ```background-repeat``` 속성에 의해 지정됩니다.

###### 예제 3

```css
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
}
```

위의 예에서는 배경 이미지가 텍스트와 동일한 위치에 배치됩니다. 텍스트에 큰 지장을 주지 않도록 이미지의 위치를 변경해 주었으면 합니다.

## background-position

```background-position``` 속성은 배경 영상의 위치를 지정하는 데 사용됩니다.

###### 예제 4

```css
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
}
```
