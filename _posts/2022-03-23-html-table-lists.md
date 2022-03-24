---
layout: post
title: HTML 16. 리스트 (Lists)
subtitle: HTML 목록을 사용하면 웹 개발자는 일련의 관련 항목을 목록으로 그룹화할 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 리스트

## 순서 없는(Unordered) HTML 리스트

순서 없는 리스트는 ```<ul>``` 태그로 시작합니다. 각 목록 항목은 ```<li>``` 태그로 시작합니다.

목록 항목은 기본적으로 글머리 기호(작은 검은색 원)로 표시됩니다.

###### 예제 1

```html
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

## 순서 있는(Ordered) HTML 리스트

순서 리스트는 ```<ol>``` 태그로 시작합니다. 각 목록 항목은 ```<li>``` 태그로 시작합니다.

목록 항목은 기본적으로 숫자로 표시됩니다.

###### 예제 2

```html
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

## HTML 설명(Description) 리스트

HTML은 설명 목록도 지원합니다.

설명 목록은 각 용어에 대한 설명이 포함된 용어 목록입니다.

```<dl>``` 태그는 설명 목록을 정의하고 ```<dt>``` 태그는 용어(이름)를 정의하고 ```<dd>``` 태그는 각 용어를 설명합니다.

###### 예제 3

```html
<dl>
  <dt>Coffee</dt>
  <dd>- black hot drink</dd>
  <dt>Milk</dt>
  <dd>- white cold drink</dd>
</dl>
```

