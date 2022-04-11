---
layout: post
title: CSS 44. 둥근 모서리 (Rounded Corners)
subtitle: CSS border-radius 속성을 사용하면 모든 요소에 "둥근 모서리"를 지정할 수 있습니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 둥근 모서리


## border-radius 속성

```border-radius``` 속성은 요소의 모서리 반지름을 정의합니다.

**Tip:** 이 속성을 사용하면 둥근 모서리를 요소에 추가할 수 있습니다!

###### 예제 1

```css
#rcorners1 {
  border-radius: 25px;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}

#rcorners2 {
  border-radius: 25px;
  border: 2px solid #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}

#rcorners3 {
  border-radius: 25px;
  background: url(paper.gif);
  background-position: left top;
  background-repeat: repeat;
  padding: 20px;
  width: 200px;
  height: 150px;
}
```

{: .box-note}
**Tip:** ```border-radius``` 속성은 실제로 ```border-top-left-radius```, ```border-top-right-radius```, ```border-bottom-right-radius```, ```border-bottom-left-radius``` 속성입니다.

## border-radius - 각 모서리 지정

```border-radius``` 속성은 1~4개의 값을 가질 수 있습니다. 규칙은 다음과 같습니다.

**4개 값 - border-radius: 15px 50px 30px 5px;** - 첫 번째 값은 왼쪽 상단 모서리에 적용되고, 두 번째 값은 오른쪽 상단 모서리에 적용되며, 세 번째 값은 오른쪽 하단 모서리에 적용되며, 네 번째 값은 왼쪽 하단 모서리에 적용됩니다.

**3개 값 - border-radius: 15px 50px 30px;** - 첫 번째 값은 왼쪽 상단 모서리에 적용되고, 두 번째 값은 오른쪽 상단 모서리와 왼쪽 하단 모서리에 적용되며, 세 번째 값은 오른쪽 하단 모서리에 적용됩니다.

**2개 값 - border-radius: 15px 50px;** - 첫 번째 값은 왼쪽 상단 및 오른쪽 하단 모서리에 적용되고 두 번째 값은 오른쪽 상단 및 왼쪽 하단 모서리에 적용됩니다.

**1개 값 - border-radius: 15px;** - 네 모서리에 모두 적용됩니다.

###### 예제 2

```css
#rcorners1 {
  border-radius: 15px 50px 30px 5px;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}

#rcorners2 {
  border-radius: 15px 50px 30px;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}

#rcorners3 {
  border-radius: 15px 50px;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}

#rcorners4 {
  border-radius: 15px;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}
```

타원형 모서리를 작성할 수도 있습니다.

###### 예제 3

```css
#rcorners1 {
  border-radius: 50px / 15px;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}

#rcorners2 {
  border-radius: 15px / 50px;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}

#rcorners3 {
  border-radius: 50%;
  background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;
}
```
