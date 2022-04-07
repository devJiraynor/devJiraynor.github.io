---
layout: post
title: CSS 22. 레이아웃 포지션 (Layout Position)
subtitle: position 속성은 요소에 사용되는 위치 지정 방법 유형(정적, 상대, 고정, 절대 또는 고정)을 지정합니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 레이아웃 포지션

## position 속성

```position``` 속성은 요소에 사용되는 위치 지정 방법의 유형을 지정합니다.

다음과 같은 다섯 가지 위치 값이 있습니다.

+ ```static```
+ ```relative```
+ ```fixed```
+ ```absolute```
+ ```sticky```

상단, 하단, 왼쪽 및 오른쪽 속성을 사용하여 요소를 배치합니다. 그러나 이러한 속성은 위치 ```position```을 먼저 설정하지 않으면 작동하지 않습니다. 또한 위치 값에 따라 다르게 작동합니다.

## position: static;

HTML 요소는 기본적으로 정적으로 배치됩니다.

정적 위치 요소는 상단, 하단, 왼쪽 및 오른쪽 속성의 영향을 받지 않습니다.

```position: static;```가 있는 요소는 특별한 방법으로 배치되지 않으며, 항상 페이지의 정상적인 흐름에 따라 배치됩니다.

###### 예제 1

```css
div.static {
  position: static;
  border: 3px solid #73AD21;
}
```

## position: relative;

```position: relative;```가 있는 요소는 정상 위치를 기준으로 배치됩니다.

상대적으로 위치한 요소의 상단, 오른쪽, 하단 및 왼쪽 속성을 설정하면 요소가 정상 위치에서 벗어나 조정됩니다. 다른 컨텐츠는 요소가 남긴 갭에 맞게 조정되지 않습니다.

###### 예제 2

```css
div.relative {
  position: relative;
  left: 30px;
  border: 3px solid #73AD21;
}
```

## position: fixed;

```position: fixed;```가 있는 요소는 뷰포트를 기준으로 배치되며, 이는 페이지가 스크롤되더라도 항상 같은 위치에 유지됨을 의미합니다. 상단, 오른쪽, 하단 및 왼쪽 속성은 요소를 배치하는 데 사용됩니다.

고정 요소는 페이지에 일반적으로 위치했을 때 공백이 생기지 않습니다.

페이지의 오른쪽 아래 모서리에 있는 고정 요소를 주목하십시오. 사용되는 CSS는 다음과 같습니다.

###### 예제 3

```css
div.fixed {
  position: fixed;
  bottom: 0;
  right: 0;
  width: 300px;
  border: 3px solid #73AD21;
}
```

## position: absolute;

```position: absolute;```가 있는 요소는 (고정된 것과 같이 뷰포트를 기준으로 배치되는 대신) 가장 가까운 위치에 있는 상위 요소에 대해 상대적으로 배치됩니다.

그러나 절대 위치 지정 요소가 위치 지정 상위 요소가 없는 경우, 문서 본문을 사용하고 페이지 스크롤과 함께 이동합니다.

**Note:** 절대 위치 요소는 일반 흐름에서 제거되며 요소가 겹칠 수 있습니다.

###### 예제 4

```css
div.relative {
  position: relative;
  width: 400px;
  height: 200px;
  border: 3px solid #73AD21;
}

div.absolute {
  position: absolute;
  top: 80px;
  right: 0;
  width: 200px;
  height: 100px;
  border: 3px solid #73AD21;
}
```

## position: sticky;

```position: sticky;```가 있는 요소는 사용자의 스크롤 위치를 기준으로 배치됩니다.

고정 요소는 스크롤 위치에 따라 ```relative``` 요소와 ```fixed``` 요소를 전환합니다. 뷰포트에서 지정된 오프셋 위치가 충족될 때까지 상대적인 위치에 배치됩니다. 그런 다음 제자리에 고정됩니다(위치:고정됨).

{: .box-note}
**Note:** Internet Explorer는 고정 위치를 지원하지 않습니다. Safari에는 -webkit- 접두사가 필요합니다(아래 예제 참조). 또한 고정 위치가 작동하려면 ```top```, ```right```, ```bottom``` 또는 ```left``` 중 하나 이상을 지정해야 합니다.

이 예에서 스틱 요소는 스크롤 위치에 도달하면 페이지 맨 위(```top: 0```)에 부착됩니다.

###### 예제 5

```css
div.sticky {
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
  background-color: green;
  border: 2px solid #4CAF50;
}
```
