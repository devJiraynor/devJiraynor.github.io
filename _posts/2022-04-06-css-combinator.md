---
layout: post
title: CSS 28. 콤비네이터 (Combinators)
subtitle: 콤비네이터는 셀렉터 간의 관계를 설명하는 것입니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 콤비네이터

## 콤비네이터

CSS 셀렉터는 둘 이상의 단순 셀렉터를 포함할 수 있습니다. 간단한 셀렉터 사이에 콤비네이터를 포함할 수 있습니다.

CSS에는 네 가지 다른 조합이 있습니다.

+ 자손 섹렉터(space)
+ 자식 섹렉터(>)
+ 인접 형제 섹렉터(+)
+ 일반 형제 섹렉터(~)

## 자손 섹렉터

자손 섹렉터는 지정된 요소의 하위 요소인 모든 요소와 일치합니다.

다음 예제에서는 ```<div>``` 요소 내부의 모든 ```<p>``` 요소를 선택합니다.

###### 예제 1

```css
div p {
  background-color: yellow;
}
```

## 자식 섹렉터 (>)

자식 섹렉터는 지정된 요소의 자식인 모든 요소를 선택합니다.

다음 예제에서는 ```<div>``` 요소의 하위 요소인 모든 ```<p>``` 요소를 선택합니다.

###### 예제 2

```css
div > p {
  background-color: yellow;
}
```

## 인접 형제 섹렉터(+)

인접 형제 섹렉터는 다른 특정 요소 바로 뒤에 있는 요소를 선택하는 데 사용됩니다.

형제 요소는 동일한 상위 요소를 가져야 하며 "인접"은 "바로 다음"을 의미합니다.

다음 예제에서는 ```<div>``` 요소 바로 뒤에 배치되는 첫 번째 ```<p>``` 요소를 선택합니다.

###### 예제 3

```css
div + p {
  background-color: yellow;
}
```

## 일반 형제 셀렉터(~)

일반 형제 셀렉터는 지정된 요소의 다음 형제인 모든 요소를 선택합니다.

다음 예제에서는 ```<div>``` 요소의 다음 형제인 모든 ```<p>``` 요소를 선택합니다.

###### 예제 4

```css
div ~ p {
  background-color: yellow;
}
```

