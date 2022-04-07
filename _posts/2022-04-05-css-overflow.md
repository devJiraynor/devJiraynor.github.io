---
layout: post
title: CSS 24. Overflow
subtitle: CSS overflow 속성은 너무 커서 영역에 맞지 않는 콘텐츠에 대한 작업을 제어합니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 레이아웃 Overflow

## 오버플로우

```overflow``` 속성은 요소의 내용이 너무 커서 지정된 영역에 맞지 않을 때 내용을 클리핑할지 또는 스크롤 막대를 추가할지 여부를 지정합니다.

```overflow``` 속성의 값은 다음과 같습니다.

+ ```visible``` - 기본값. 오버플로가 잘리지 않습니다. 내용이 요소의 상자 외부에 렌더링됩니다.
+ ```hidden``` - 오버플로가 잘리고 나머지 내용이 보이지 않습니다.
+ ```scroll``` - 오버플로가 잘리고 스크롤 막대가 추가되어 나머지 내용을 볼 수 있습니다.
+ ```auto``` - 스크롤과 비슷하지만 필요한 경우에만 스크롤 막대를 추가합니다.

**Note:** ```overflow``` 속성은 지정된 높이를 가진 블록 요소에만 적용됩니다.
**Note:** OS X Lion(Mac)에서는 스크롤바가 기본적으로 숨겨져 있으며 "overflow:scroll"이 설정되었음에도 불구하고 사용할 때만 표시됩니다.

## overflow: visible

기본적으로 오버플로가 ```visible```로, 오버플로는 잘리지 않고 요소의 상자 외부에 렌더링됩니다.

###### 예제 1

```css
div {
  width: 200px;
  height: 65px;
  background-color: coral;
  overflow: visible;
}
```

## overflow: hidden

```hidden```을 사용하면 오버플로가 잘리고 나머지 내용이 숨겨집니다.

###### 예제 2

```css
div {
  overflow: hidden;
}
```

## overflow: scroll

값을 ```scroll```으로 설정하면 오버플로가 잘리고 스크롤 막대가 추가되어 상자 안으로 스크롤됩니다. 이렇게 하면 스크롤 막대가 수평 및 수직으로 추가됩니다(필요 없는 경우에도).

###### 예제 3

```css
div {
  overflow: scroll;
}
```

## overflow: auto

```auto``` 값은 ```scroll```과 비슷하지만 필요한 경우에만 스크롤 막대를 추가합니다.

###### 예제 4

```css
div {
  overflow: auto;
}
```

## overflow-x 와 overflow-y

```overflow-x``` 및 ```overflow-y``` 속성은 콘텐츠의 오버플로를 수평 또는 수직(또는 둘 다)으로 변경할지 여부를 지정합니다.

```overflow-x```는 내용의 왼쪽/오른쪽 모서리로 수행할 작업을 지정합니다.
```overflow-y```는 내용의 위쪽/아래쪽 모서리로 수행할 작업을 지정합니다.

###### 예제 5

```css
div {
  overflow-x: hidden; /* Hide horizontal scrollbar */
  overflow-y: scroll; /* Add vertical scrollbar */
}
```
