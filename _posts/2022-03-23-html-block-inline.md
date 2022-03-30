---
layout: post
title: HTML 17. 블록 및 인라인 요소 (Block and Inline Elements)
subtitle: 모든 HTML 요소에는 요소의 유형에 따라 기본 표시 값이 있습니다. 표시값에는 block과 inline의 2가지가 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 블록(Block) 및 인라인(Inline) 요소

## 블록 요소

블록 레벨 요소는 항상 새 행에서 시작되며 브라우저는 요소 앞뒤에 일부 공간(여백)을 자동으로 추가합니다.

블록 레벨 요소는 항상 사용 가능한 전체 폭을 차지합니다(가능한 한 왼쪽과 오른쪽으로 늘어짐).

일반적으로 사용되는 블록 요소는 ```<p>``` 와 ```<div>``` 입니다.

```<p>``` 요소는 HTML 문서의 문단을 정의합니다.

```<div>``` 요소는 HTML 문서에서 분할 또는 섹션을 정의합니다.

###### 예제 1

```html
<p>Hello World</p>
<div>Hello World</div>
```

HTML의 블록 레벨 요소는 다음과 같습니다.

```<address>``` ```<article>``` ```<aside>``` ```<blockquote>```
```<canvas>``` ```<dd>``` ```<div>``` ```<dl>``` 
```<dt>``` ```<fieldset>``` ```<figcaption>``` ```<figure>``` 
```<footer>``` ```<form>``` ```<h1>-<h6>``` ```<header>``` 
```<hr>``` ```<li>``` ```<main>``` ```<nav>``` 
```<noscript>``` ```<ol>``` ```<p>``` ```<pre>``` 
```<section>``` ```<table>``` ```<tfoot>``` ```<ul>``` ```<video>```

## 인라인 요소

인라인 요소는 새 행에서 시작되지 않습니다.

인라인 요소는 필요한 만큼만 너비를 차지합니다.

###### 예제 2

```html
<span>Hello World</span>
```

HTML 의 인라인 요소는 다음과 같습니다.

```<a>``` ```<abbr>``` ```<acronym>``` ```<b>```
```<bdo>``` ```<big>``` ```<br>``` ```<button>```
```<cite>``` ```<code>``` ```<dfn>``` ```<em>```
```<i>``` ```<img>``` ```<input>``` ```<kbd>```
```<label>``` ```<map>``` ```<object>``` ```<output>```
```<q>``` ```<samp>``` ```<script>``` ```<select>```
```<small>``` ```<span>``` ```<strong>``` ```<sub>```
```<sup>``` ```<textarea>``` ```<time>``` ```<tt>``` 
```<var>```

{: .box-note}
**Note:** 인라인 요소는 블록 수준 요소를 포함할 수 없습니다!

## ```<div>``` 요소

```<div>``` 요소는 종종 다른 HTML 요소의 컨테이너로 사용됩니다.

```<div>``` 요소에는 필수 속성이 없지만 ```style```, ```class``` 및 ```id``` 가 공통입니다.

CSS와 함께 사용하면 ```<div>``` 요소를 사용하여 콘텐츠 블록을 스타일링할 수 있습니다.

###### 예제 3

```html
<div style="background-color:black;color:white;padding:20px;">
  <h2>London</h2>
  <p>London is the capital city of England. It is the most populous city in the United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
</div>
```

## ```<span>``` 요소

```<span>``` 요소는 텍스트의 일부 또는 문서의 일부를 표시하기 위해 사용되는 인라인 컨테이너입니다.

```<span>``` 요소에는 필수 속성이 없지만 ```style```, ```class``` 및 ```id``` 가 공통입니다.

CSS와 함께 사용하면 ```<span>``` 요소를 사용하여 텍스트의 일부를 스타일링할 수 있습니다.

###### 예제 4

```html
<p>
  My mother has <span style="color:blue;font-weight:bold">blue</span> 
  eyes and my father has <span style="color:darkolivegreen;font-weight:bold">dark green</span> eyes.
</p>
```

## Summary

+ 표시값에는 block과 inline의 2가지가 있습니다.
+ 블록 레벨 요소는 항상 새 라인에서 시작하여 사용 가능한 전체 너비를 차지합니다.
+ 인라인 요소는 새 줄에서 시작하지 않으며 필요한 만큼만 너비를 차지합니다.
+ ```<div>``` 요소는 블록 수준이며 다른 HTML 요소의 컨테이너로 자주 사용됩니다.
+ ```<span>``` 요소는 텍스트의 일부 또는 문서의 일부를 표시하기 위해 사용되는 인라인 컨테이너입니다.
