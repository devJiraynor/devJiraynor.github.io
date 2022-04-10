---
layout: post
title: CSS 31. 불투명도/투명도 (Opacity / Transparency)
subtitle: opacity 속성은 요소의 불투명도/투명도를 지정합니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 불투명도/투명도 (Opacity / Transparency)

## 투명 이미지

```opacity``` 속성은 0.0 - 1.0 사이의 값을 가질 수 있습니다. 값이 낮을수록 투명합니다.

###### 예제 1

```css
img {
  opacity: 0.5;
}
```

## 투명 호버 효과

```opacity``` 속성은 마우스 오버 시 불투명도를 변경하기 위해 ```:hover``` 셀렉터와 함께 종종 사용됩니다.

###### 예제 2

```css
img {
  opacity: 0.5;
}

img:hover {
  opacity: 1.0;
}
```

## 투명 박스

```opacity``` 속성을 사용하여 요소의 배경에 투명도를 추가하면 모든 하위 요소가 동일한 투명도를 상속합니다. 이렇게 하면 완전히 투명한 요소 내부의 텍스트를 읽기 어렵게 만들 수 있습니다.

