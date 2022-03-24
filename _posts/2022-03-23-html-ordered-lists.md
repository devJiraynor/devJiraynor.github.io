---
layout: post
title: HTML 16-2. 순서 있는 리스트 (Ordered Lists)
subtitle: HTML ol 태그는 순서 리스트를 정의합니다. 순서부 리스트는 숫자 또는 알파벳 순으로 지정할 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 순서 있는 리스트

## 순서 있는 HTML 리스트

순서 리스트는 ```<ol>``` 태그로 시작합니다. 각 목록 항목은 ```<li>``` 태그로 시작합니다.

목록 항목은 기본적으로 숫자로 표시됩니다.

###### 예제 1

```html
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

## 순서 있는 HTML 리스트 - Type 속성

```<ol>``` 태그의 ```type``` 속성은 목록 항목 마커의 유형을 정의합니다.

| 타입 | 설명 |
| type="1" | 리스트 항목에는 번호가 매겨집니다(기본값). |
| type="A" | 리스트 항목에는 대문자로 번호가 매겨집니다. |
| type="a" | 리스트 항목에는 소문자로 번호가 매겨집니다. |
| type="I" | 리스트 항목에는 대문자 로마 번호가 매겨집니다. |
| type="i" | 리스트 항목에는 소문자 로마 숫자로 번호가 매겨집니다. |

###### 예제 2 - 번호

```html
<ol type="1">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

###### 예제 2 - 대문자 영어

```html
<ol type="A">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

###### 예제 2 - 소문자 영어

```html
<ol type="a">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

###### 예제 2 - 대문자 로마 숫자

```html
<ol type="I">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

###### 예제 2 - 소문자 로마 숫자

```html
<ol type="i">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

## 리스트 카운팅 제어

기본적으로는 순서 목록은 1부터 카운트를 시작합니다. 지정된 수부터 카운트를 시작하려면 ```start``` 속성을 사용할 수 있습니다.

###### 예제 3

```html
<ol start="50">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

## HTML 리스트 중첩

목록을 중첩할 수 있습니다.(리스트 내부)

###### 예제 4

```html
<ol>
  <li>Coffee</li>
  <li>Tea
    <ol>
      <li>Black tea</li>
      <li>Green tea</li>
    </ol>
  </li>
  <li>Milk</li>
</ol>
```

{: .box-note}
**Note:** 리스트 항목(```<li>```)에는, 새로운 리스트와 그 외의 HTML 요소(이미지나 링크등)를 포함할 수 있습니다.

## Summary

+ HTML ```<ol>``` 요소를 사용하여 순서 목록을 정의합니다.
+ HTML ```type``` 속성을 사용하여 번호 유형을 정의합니다.
+ HTML ```<li>``` 요소를 사용하여 목록 항목을 정의합니다.
+ 리스트는 네스트 할 수 있습니다.
+ 목록 항목은 다른 HTML 요소를 포함할 수 있습니다.
