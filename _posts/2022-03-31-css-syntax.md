---
layout: post
title: CSS 02. 구문 (Syntax)
subtitle: CSS 규칙은 셀렉터와 선언 블록으로 구성됩니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 구문 

## CSS 구문

```css
셀렉터 { 프로퍼티: 값; 프로퍼티: 값;}
```

프로퍼티: 값 = 선언블록

셀렉터는 스타일을 지정할 HTML 요소를 가리킵니다.

선언 블록에는 세미콜론으로 구분된 선언이 하나 이상 포함되어 있습니다.

각 선언에는 콜론으로 구분된 CSS 속성명과 값이 포함됩니다.

여러 CSS 선언은 세미콜론으로 구분되며 선언 블록은 중괄호로 둘러싸여 있습니다.

###### 예제 1 - 이 예에서는 모든 ```<p>``` 요소가 빨간색 텍스트 색상으로 가운데 정렬됩니다.

```css
p {
  color: red;
  text-align: center;
}
```

예제 설명:

+ ```p```는 CSS의 셀렉터입니다(스타일링하는 HTML 요소 ```<p>```를 가리킵니다).
+ ```color```는 속성이고 ```red```는 속성 값입니다.
+ ```text-align```은 속성이고 ```center```는 속성 값입니다.
