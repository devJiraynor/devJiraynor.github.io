---
layout: post
title: CSS 09. Margin
subtitle: margin은 정의된 테두리 밖에서 요소 주위에 공간을 만드는 데 사용됩니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS Margin

## margin

CSS ```margin``` 속성은 정의된 테두리 외부에 요소 주위의 여백을 작성하기 위해 사용됩니다.

CSS를 사용하면 margin을 완전히 제어할 수 있습니다. 요소의 각 변(위, 오른쪽, 아래 및 왼쪽)에 대한 여백을 설정하는 속성이 있습니다.

## margin - 각 측면

CSS에는 요소의 각 측면에 대한 여백을 지정하는 속성이 있습니다.

+ ```margin-top```
+ ```margin-right```
+ ```margin-bottom```
+ ```margin-left```

모든 ```margin``` 속성은 다음 값을 가질 수 있습니다.

+ auto - 브라우저가 여백을 계산합니다.
+ length - px, pt, cm 등의 여백을 지정합니다.
+ % - 포함 요소 폭의 % 단위로 여백을 지정합니다.
+ inherit - 부모 요소에서 여백을 상속하도록 지정합니다.

**Tip:** 음수 값을 사용할 수 있습니다.

###### 예제 1

```css
p {
  margin-top: 100px;
  margin-bottom: 100px;
  margin-right: 150px;
  margin-left: 80px;
}
```

## margin - 축약 속성

코드를 단축하기 위해 하나의 속성에서 모든 여백 속성을 지정할 수 있습니다.

```margin``` 속성은 다음과 같은 개별 ```margin``` 속성에 대한 줄임말 속성입니다.

+ ```margin-top```
+ ```margin-right```
+ ```margin-bottom```
+ ```margin-left```

동작은 다음과 같습니다.

```margin``` 속성에 4개의 값이 있는 경우:

+ **margin: 25px 50px 75px 100px;**
- 상단여백 25px
- 우측여백 50px
- 하단여백 75px
- 왼쪽여백 100px

###### 예제 2

```css
p {
  margin: 25px 50px 75px 100px;
}
```

```margin``` 속성에 3개의 값이 있는 경우:

+ **margin: 25px 50px 75px;**
- 상단여백 25px
- 좌우여백 50px
- 하단여백 75px

###### 예제 3

```css
p {
  margin: 25px 50px 75px;
}
```

```margin``` 속성에 2개의 값이 있는 경우:

+ **margin: 25px 50px;**
- 상하여백 25px
- 좌우여백 50px

###### 예제 4

```css
p {
  margin: 25px 50px;
}
```

```margin``` 속성에 1개의 값이 있는 경우:

+ **margin: 25px;**
- 전체여백 25px

###### 예제 5

```css
p {
  margin: 25px;
}
```

## auto 값

```margin``` 특성을 ```auto```로 설정하여 컨테이너 내에서 요소를 수평으로 중앙에 배치할 수 있습니다.

그러면 요소가 지정된 너비를 차지하고 나머지 공간은 왼쪽과 오른쪽 여백으로 균등하게 분할됩니다.

###### 예제 6

```css
div {
  width: 300px;
  margin: auto;
  border: 1px solid red;
}
```

## inherit 값

다음 예제에서는 ```<p class="ex1">``` 요소의 왼쪽 여백을 부모 요소(```<div>```)에서 상속할 수 있습니다.

###### 예제 7

```css
div {
  border: 1px solid red;
  margin-left: 100px;
}

p.ex1 {
  margin-left: inherit;
}
```

## margin collapse

요소의 상단 및 하단 여백이 두 여백 중 가장 큰 여백과 동일한 단일 여백으로 축소되는 경우가 있습니다.

이것은 좌우 여백에 발생하지 않습니다.

###### 예제 8

```css
h1 {
  margin: 0 0 50px 0;
}

h2 {
  margin: 20px 0 0 0;
}
```

위의 예에서는 ```<h1>``` 요소의 하단 여백은 50px, ```<h2>``` 요소의 상단 여백은 20px로 설정되어 있습니다.

상식적으로 ```<h1>```과 ```<h2>``` 사이의 수직 마진은 총 70px(50px + 20px)가 될 것으로 생각됩니다. 그러나 마진붕괴로 인해 실제 마진은 50px가 됩니다.
