---
layout: post
title: CSS 20. 디스플레이 (Display)
subtitle: 디스플레이 속성은 레이아웃을 제어하는 가장 중요한 CSS 속성입니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 레이아웃 display 속성

## display 속성

```display``` 속성은 요소의 표시 여부/방법을 지정합니다.

모든 HTML 요소는 요소 유형에 따라 기본 표시 값을 가집니다. 대부분의 요소의 기본 표시 값은 ```block``` 또는 ```inline```입니다.

## block 레벨 요소

블록 레벨 요소는 항상 새 줄에서 시작하여 사용 가능한 전체 너비를 차지합니다(가능한 한 왼쪽과 오른쪽으로 확장).

블록 레벨 요소의 예:

+ ```<div>```
+ ```<h1> - <h6>```
+ ```<p>```
+ ```<form>```
+ ```<header>```
+ ```<footer>```
+ ```<section>```

## 인라인 요소

인라인 요소는 새 줄에서 시작되지 않으며 필요한 만큼의 너비만 사용합니다.

인라인 요소의 예:

+ ```<span>```
+ ```<a>```
+ ```<img>```

## Display: none;

```display: none;```는 자바스크립트에서 요소를 삭제하고 다시 생성하지 않고 요소를 숨기고 표시하기 위해 일반적으로 사용된다. 이 작업을 수행할 수 있는 방법을 알고 싶다면 이 페이지의 마지막 예를 참조하십시오.

```<script>``` 요소는 ```display: none;```를 기본값으로 사용합니다.

## 기본 표시 값 재정의
