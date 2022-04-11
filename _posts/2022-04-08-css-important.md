---
layout: post
title: CSS 42. !important 규칙
subtitle: CSS의 !important 규칙은 속성/값에 정상보다 더 많은 중요도를 추가하는 데 사용됩니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS !important 규칙

## !important 란?

CSS의 ```!important``` 규칙은 속성/값에 정상보다 더 많은 중요도를 추가하는 데 사용됩니다.

실제로 ```!important``` 규칙을 사용하면 해당 요소의 특정 속성에 대한 이전 스타일링 규칙이 모두 재정의됩니다!

###### 예제 1

```css
#myid {
  background-color: blue;
}

.myclass {
  background-color: gray;
}

p {
  background-color: red !important;
}
```

예제 설명 : 

위의 예에서 ID 셀렉터와 클래스 셀렉터가 더 높은 특이도을 가지더라도 세 문단 모두 빨간색 배경색을 갖게 됩니다. ```!important``` 규칙은 두 경우 모두 ```background-color``` 속성을 재정의합니다.
