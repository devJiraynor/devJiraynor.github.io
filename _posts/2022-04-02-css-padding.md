---
layout: post
title: CSS 10. Padding
subtitle: padding은 정의된 테두리 안쪽에 요소의 내용 주위에 공간을 만드는 데 사용됩니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS Padding

## padding

CSS ```padding``` 속성은 정의된 테두리 내에서 요소의 내용 주위에 여백을 생성하기 위해 사용됩니다.

CSS를 사용하면 패딩을 완전히 제어할 수 있습니다. 요소의 각 면(위, 오른쪽, 아래 및 왼쪽)에 대한 패딩을 설정하는 속성이 있습니다.

## padding - 각 측면

CSS에는 요소의 각 측면에 대한 패딩을 지정하는 속성이 있습니다.

+ ```padding-top```
+ ```padding-right```
+ ```padding-bottom```
+ ```padding-left```

모든 ```padding``` 속성은 다음 값을 가질 수 있습니다.

+ length - px, pt, cm 등의 여백을 지정합니다.
+ % - 포함 요소 폭의 % 단위로 여백을 지정합니다.
+ inherit - 부모 요소에서 여백을 상속하도록 지정합니다.

**Tip:** 음수 값을 사용할 수 없습니다.

###### 예제 1

```css
div {
  padding-top: 50px;
  padding-right: 30px;
  padding-bottom: 50px;
  padding-left: 80px;
}
```

## padding - 축약 속성

코드를 단축하기 위해 하나의 속성에 모든 패딩 속성을 지정할 수 있습니다.

패딩 속성은 다음과 같은 개별 패딩 속성의 약어 속성입니다.

+ ```padding-top```
+ ```padding-right```
+ ```padding-bottom```
+ ```padding-left```

동작은 다음과 같습니다.

```padding``` 속성에 4개의 값이 있는 경우:

+ **padding: 25px 50px 75px 100px;**
- 상단패딩 25px
- 우측패딩 50px
- 하단패딩 75px
- 왼쪽패딩 100px

###### 예제 2

```css
div {
  padding: 25px 50px 75px 100px;
}
```

```padding``` 속성에 3개의 값이 있는 경우:

+ **padding: 25px 50px 75px;**
- 상단패딩 25px
- 좌우패딩 50px
- 하단패딩 75px

###### 예제 3

```css
div {
  padding: 25px 50px 75px;
}
```

```padding``` 속성에 2개의 값이 있는 경우:

+ **padding: 25px 50px;**
- 상하패딩 25px
- 좌우패딩 50px

###### 예제 4

```css
div {
  padding: 25px 50px;
}
```

```padding``` 속성에 1개의 값이 있는 경우:

+ **padding: 25px;**
- 전체패딩 25px

###### 예제 5

```css
div {
  padding: 25px;
}
```

## padding과 요소 너비

CSS ```width``` 속성은 요소의 콘텐츠 영역 폭을 지정합니다. 내용 영역은 요소(상자 모델)의 패딩, 테두리 및 여백 내부 부분입니다.

따라서 요소의 너비가 지정된 경우 해당 요소에 추가된 패딩이 요소의 전체 너비에 추가됩니다. 이것은 종종 바람직하지 않은 결과를 초래합니다.


###### 예제 6 - 여기서 ```<div>``` 요소에는 300px의 폭이 부여됩니다. 단, ```<div>``` 요소의 실제 폭은 350px(300px + 왼쪽 패딩 25px + 오른쪽 패딩 25px)입니다.

```
div {
  width: 300px;
  padding: 25px;
}
```

너비를 300px로 유지하려면 패딩의 양에 관계없이 ```box-size``` 속성을 사용할 수 있습니다. 이렇게 하면 요소는 실제 너비를 유지합니다. 패딩을 늘리면 사용 가능한 컨텐츠 공간이 줄어듭니다.
