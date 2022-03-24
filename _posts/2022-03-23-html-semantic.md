---
layout: post
title: HTML 27. 시맨틱 (Semantic)
subtitle: 시맨틱 요소 = 의미가 있는 요소.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 시맨틱 요소

## 시맨틱 요소란?

시맨틱 요소는 브라우저와 개발자 모두에게 의미에 대해 명확하게 설명합니다.

**non-semantic 요소**의 예: ```<div>``` 및 ```<span>``` - 내용에 대해서는 아무것도 알리지 않습니다.

**semantic 요소**의 예: ```<form>```, ```<table>``` 및 ```<article>``` - 내용을 명확하게 정의합니다.

## HTML의 시맨틱 요소

많은 웹 사이트에는 ```navigation```, ```header``` 및 ```footer``` 를 나타내기 위해 다음과 같은 HTML 코드가 포함되어 있습니다.

```<div id = "nav"> <div class = "filter"> <div id = "footer">```

HTML 에는 웹 페이지의 다른 부분을 정의하기 위해서 사용할 수 있는 시맨틱 요소가 몇 가지 있습니다.

![html_layout_01](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_layout_01.gif?raw=true)

+ ```<article>```
+ ```<aside>```
+ ```<details>```
+ ``<figcaption>```
+ ```<figure>```
+ ```<footer>```
+ ```<header>```
+ ```<main>```
+ ```<mark>```
+ ```<nav>```
+ ```<section>```
+ ```<summary>```
+ ```<time>```

## HTML ```<section>``` 요소

```<section>``` 요소는 문서의 섹션을 정의합니다.

W3C의 HTML 문서에 따르면 "섹션은 콘텐츠의 주제 그룹이며, 일반적으로 제목이 붙어 있습니다."

```<section>``` 요소를 사용할 수 있는 장소의 예를 다음에 나타냅니다.

+ 챕터
+ 서론
+ 뉴스 항목
+ 연락처 정보

웹 페이지는 일반적으로 소개, 내용 및 연락처 정보를 위한 섹션으로 분할할 수 있습니다.

###### 예제 1

```html
<section>
<h1>WWF</h1>
<p>The World Wide Fund for Nature (WWF) is an international organization working on issues regarding the conservation, research and restoration of the environment, formerly named the World Wildlife Fund. WWF was founded in 1961.</p>
</section>

<section>
<h1>WWF's Panda symbol</h1>
<p>The Panda has become the symbol of WWF. The well-known panda logo of WWF originated from a panda named Chi Chi that was transferred from the Beijing Zoo to the London Zoo in the same year of the establishment of WWF.</p>
</section>
```

## 
