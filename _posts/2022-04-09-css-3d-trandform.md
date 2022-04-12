---
layout: post
title: CSS 54. 3D 변환 (3D Transforms)
subtitle: CSS 3D 변환에 대해 알아봅니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 3D 변환

## 3D 변환

이 장에서는 다음 CSS 속성에 대해 학습합니다.

+ ```transform```

## 지원 브라우저

표의 숫자는 속성을 완전히 지원하는 최소 브라우저 버전을 지정합니다.

| 브라우저 | 구글 Chrome | 마이크로소프트 Edge | Firefox | Safari | Opera |
| 버전 | 36.0 | 10.0 | 16.0 | 9.0 | 23.0 |

## 3D 변환 메서드

```transform``` 속성을 사용하여 다음과 같은 3D 변환 방법을 사용할 수 있습니다.

+ ```rotateX()```
+ ```rotateY()```
+ ```rotateZ()```

## rotateX()

```rotateX()``` 메서드는 X축을 중심으로 요소를 주어진 각도로 회전시킵니다.

###### 예제 1

```css
#myDiv {
  transform: rotateX(150deg);
}
```

## rotateY()

```rotateY()``` 메서드는 Y축을 중심으로 요소를 주어진 각도로 회전시킵니다.

###### 예제 2

```css
#myDiv {
  transform: rotateY(150deg);
}
```

## rotateZ()

```rotateZ()``` 메서드는 요소를 Z축을 중심으로 주어진 각도로 회전시킵니다.

###### 예제 3

```css
#myDiv {
  transform: rotateZ(90deg);
}
```
