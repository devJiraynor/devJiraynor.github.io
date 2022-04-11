---
layout: post
title: CSS 45. 테두리 이미지 (Border Image)
subtitle: CSS border-image 속성을 사용하여 요소 주위의 테두리로 사용할 이미지를 설정할 수 있습니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 테두리 이미지

## border-image 속성

CSS ```border-image``` 속성을 사용하면 요소 주위의 일반 테두리 대신 사용할 이미지를 지정할 수 있습니다.

속성은 세 부분으로 구성됩니다.

+ 테두리로 사용할 이미지
+ 이미지를 자를 위치
+ 중간 섹션을 반복할지 또는 연장할지 정의

```border-image``` 속성은 이미지를 가져와서 tic-tac-toe 보드처럼 9개의 섹션으로 잘라냅니다. 그런 다음 모서리를 모서리에 배치하고 가운데 부분은 지정한 대로 반복되거나 늘어납니다.

**Note:** ```border-image```가 작동하려면 ```border``` 속성을 설정해야 합니다!

###### 예제 1

```css
#borderimg {
  border: 10px solid transparent;
  padding: 15px;
  border-image: url(border.png) 30 round;
}
```

###### 예제 2

```css
#borderimg {
  border: 10px solid transparent;
  padding: 15px;
  border-image: url(border.png) 30 stretch;
}
```

{: .box-note}
**Tip:** ```border-image``` 속성은 실제로 ```border-image-source```, ```border-image-slice```, ```border-image-width```, ```border-image-outset```, ```border-image-repeat``` 속성에 대한 간략한 속성입니다.
