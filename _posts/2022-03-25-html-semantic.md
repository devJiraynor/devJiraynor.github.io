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

## HTML ```<article>``` 요소

```<article>``` 요소는 독립적이고 자기 완결된 콘텐츠를 지정합니다.

기사는 그 자체로 의미가 있어야 하며, 다른 웹사이트와는 독립적으로 배포할 수 있어야 합니다.

```<article>``` 요소를 사용할 수 있는 예:

+ 포럼 투고
+ 블로그 투고
+ 사용자 코멘트
+ 제품 카드
+ 신문 기사

###### 예제 2

```html
<article>
<h2>Google Chrome</h2>
<p>Google Chrome is a web browser developed by Google, released in 2008. Chrome is the world's most popular web browser today!</p>
</article>

<article>
<h2>Mozilla Firefox</h2>
<p>Mozilla Firefox is an open-source web browser developed by Mozilla. Firefox has been the second most popular web browser since January, 2018.</p>
</article>

<article>
<h2>Microsoft Edge</h2>
<p>Microsoft Edge is a web browser developed by Microsoft, released in 2015. Microsoft Edge replaced Internet Explorer.</p>
</article>
```

###### 예제 3

```html
<html>
<head>
<style>
.all-browsers {
  margin: 0;
  padding: 5px;
  background-color: lightgray;
}

.all-browsers > h1, .browser {
  margin: 10px;
  padding: 5px;
}

.browser {
  background: white;
}

.browser > h2, p {
  margin: 4px;
  font-size: 90%;
}
</style>
</head>
<body>

<article class="all-browsers">
  <h1>Most Popular Browsers</h1>
  <article class="browser">
    <h2>Google Chrome</h2>
    <p>Google Chrome is a web browser developed by Google, released in 2008. Chrome is the world's most popular web browser today!</p>
  </article>
  <article class="browser">
    <h2>Mozilla Firefox</h2>
    <p>Mozilla Firefox is an open-source web browser developed by Mozilla. Firefox has been the second most popular web browser since January, 2018.</p>
  </article>
  <article class="browser">
    <h2>Microsoft Edge</h2>
    <p>Microsoft Edge is a web browser developed by Microsoft, released in 2015. Microsoft Edge replaced Internet Explorer.</p>
  </article>
</article>

</body>
</html>
```

## HTML ```<header>``` 요소

```<header>``` 요소는 도입 콘텐츠용 컨테이너 또는 네비게이션링크 세트를 나타냅니다.

```<header>``` 요소에는 일반적으로 다음이 포함됩니다.

+ 1개 또는 복수의 표제 요소(```<h1>-<h6>```)
+ 로고 또는 아이콘
+ 저자 정보

{: .box-note}
**Note:** 1개의 HTML 문서에 여러 개의 ```<header>``` 요소를 포함할 수 있습니다. 단, ```<header>``` 는 ```<footer>```, ```<address>``` 또는 다른 ```<header>``` 요소 내에 배치할 수 없습니다.

###### 예제 4

```html
<article>
  <header>
    <h1>What Does WWF Do?</h1>
    <p>WWF's mission:</p>
  </header>
  <p>WWF's mission is to stop the degradation of our planet's natural environment,
  and build a future in which humans live in harmony with nature.</p>
</article>
```

## HTML ```<footer>``` 요소

```<footer>``` 요소는 문서 또는 섹션의 바닥글을 정의합니다.

```<footer>``` 요소에는 일반적으로 다음이 포함됩니다.

+ 저자 정보
+ 저작권 정보
+ 연락처 정보
+ 사이트 맵
+ 홈으로 이동
+ 관련 문서

1개의 문서에 여러 개의 ```<footer>``` 요소를 포함할 수 있습니다.

###### 예제 5

```html
<footer>
  <p>Author: Hege Refsnes</p>
  <p><a href="mailto:hege@example.com">hege@example.com</a></p>
</footer>
```

## HTML ```<nav>``` 요소

```<nav>``` 요소는 네비게이션링크 세트를 정의합니다.

{: .box-note}
문서의 모든 링크가 ```<nav>``` 요소 안에 있는 것은 아닙니다. ```<nav>``` 요소는 내비게이션 링크의 주요 블록만을 대상으로 합니다. 비활성화된 사용자의 화면 판독기와 같은 브라우저는 이 요소를 사용하여 내용의 초기 렌더링을 생략할지 여부를 결정할 수 있습니다.

###### 예제 6

```html
<nav>
  <a href="/html/">HTML</a> |
  <a href="/css/">CSS</a> |
  <a href="/js/">JavaScript</a> |
  <a href="/jquery/">jQuery</a>
</nav>
```

## HTML ```<aside>``` 요소

```<aside>``` 요소는, 컨텐츠가 배치되어 있는 컨텐츠(사이드바등)와는 별도로, 몇개의 컨텐츠를 정의합니다.

```<aside>``` 콘텐츠는 주변 콘텐츠와 간접적으로 관련되어 있어야 합니다.

###### 예제 7

```html
<p>My family and I visited The Epcot center this summer. The weather was nice, and Epcot was amazing! I had a great summer together with my family!</p>

<aside>
<h4>Epcot Center</h4>
<p>Epcot is a theme park at Walt Disney World Resort featuring exciting attractions, international pavilions, award-winning fireworks and seasonal special events.</p>
</aside>
```

###### 예제 8

```html
<html>
<head>
<style>
aside {
  width: 30%;
  padding-left: 15px;
  margin-left: 15px;
  float: right;
  font-style: italic;
  background-color: lightgray;
}
</style>
</head>
<body>

<p>My family and I visited The Epcot center this summer. The weather was nice, and Epcot was amazing! I had a great summer together with my family!</p>

<aside>
<p>The Epcot center is a theme park at Walt Disney World Resort featuring exciting attractions, international pavilions, award-winning fireworks and seasonal special events.</p>
</aside>

<p>My family and I visited The Epcot center this summer. The weather was nice, and Epcot was amazing! I had a great summer together with my family!</p>
<p>My family and I visited The Epcot center this summer. The weather was nice, and Epcot was amazing! I had a great summer together with my family!</p>

</body>
</html>
```

## HTML ```<figure>``` 와 ```<figcaption>``` 요소

```<figure>``` 태그는 일러스트, 다이어그램, 사진, 코드 리스트 등 셀프 콘텐츠를 지정합니다.

```<figcaption>``` 태그는 ```<figure>``` 요소의 캡션을 정의합니다. ```<figcaption>``` 요소는 ```<figure>``` 요소의 첫 번째 자식 또는 마지막 자식으로 배치할 수 있습니다.

```<img>``` 요소는 실제 이미지/ 일러스트를 정의합니다.

###### 예제 9

```html
<figure>
  <img src="pic_trulli.jpg" alt="Trulli">
  <figcaption>Fig1. - Trulli, Puglia, Italy.</figcaption>
</figure>
```

## 왜 시맨틱 요소를 사용해야하는가?

W3C에 따르면 "시맨틱 웹을 통해 애플리케이션, 기업 및 커뮤니티에서 데이터를 공유하고 재사용할 수 있습니다." 라는 취지로 사용됩니다.
