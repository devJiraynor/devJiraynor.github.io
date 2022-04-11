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

## !important에 대한 중요 정보

```!important``` 규칙을 재정의하는 유일한 방법은 소스 코드에 동일한(또는 더 높은) 특수성을 가진 선언에 다른 ```!important``` 규칙을 포함시키는 것입니다. 여기서 문제가 시작됩니다! 이것은 CSS 코드를 혼란스럽게 만들고 디버깅은 특히 당신이 큰 스타일시트를 가지고 있다면 어려울 것입니다!

여기서 우리는 간단한 예를 만들었습니다. CSS 소스 코드를 볼 때, 어떤 색이 가장 중요하다고 생각되는지는 매우 명확하지 않습니다.

###### 예제 2

```css
#myid {
  background-color: blue !important;
}

.myclass {
  background-color: gray !important;
}

p {
  background-color: red !important;
}
```

**Tip:** ```!important``` 규칙에 대해 아는 것이 좋습니다. 일부 CSS 소스 코드에서 볼 수 있습니다. 그러나 꼭 사용해야 하는 경우가 아니면 사용하지 마십시오.

## !important의 한 가지 또는 두 가지 적절한 사용

```!important```를 사용하는 한 가지 방법은 다른 방법으로 재정의할 수 없는 스타일을 재정의해야 하는 경우입니다. CMS(Content Management System)에서 작업 중이며 CSS 코드를 편집할 수 없는 경우일 수 있습니다. 그런 다음 일부 CMS 스타일을 재정의하도록 일부 사용자 정의 스타일을 설정할 수 있습니다.

```!important```을 사용하는 또 다른 방법은 페이지의 모든 ```button```에 대해 특별한 모양을 원한다고 가정하는 것입니다. 여기서 단추는 회색 배경색, 흰색 텍스트, 일부 패딩 및 테두리로 스타일 지정됩니다.

###### 예제 3

```css
.button {
  background-color: #8c8c8c;
  color: white;
  padding: 5px;
  border: 1px solid black;
}
```

```button```의 모양은 특이도가 높은 다른 요소 안에 넣었을 때 바뀔 수 있습니다. 그러면 특성이 충돌합니다. 다음은 그 예입니다.

###### 예제 4

```css
.button {
  background-color: #8c8c8c;
  color: white;
  padding: 5px;
  border: 1px solid black;
}

#myDiv a {
  color: red;
  background-color: yellow;
}
```

모든 ```button```이 같은 모양을 가지도록 "강제"하려면, 다음과 같이 ```!important``` 규칙을 ```button``` 속성에 추가할 수 있습니다.
