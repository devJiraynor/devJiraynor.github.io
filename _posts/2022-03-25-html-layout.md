---
layout: post
title: HTML 24. 레이아웃 (Layout)
subtitle: 웹 사이트는 종종 여러 열에 내용을 표시합니다.(잡지 또는 신문 등)
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<a href="https://youtu.be/0KgAJ6CgwcA" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 24. 레이아웃 (Layout) 영상 보러가기</a>
<br>
<br>

# HTML 레이아웃 

## HTML 레이아웃 요소

HTML에는 웹 페이지의 다른 부분을 정의하는 몇 가지 시맨틱 요소가 있습니다.

![html_layout_01](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_layout_01.gif?raw=true)

+ ```<header>``` - 문서 또는 섹션의 헤더를 정의합니다.
+ ```<nav>``` - 네비게이션링크 세트를 정의합니다.
+ ```<section>``` - 문서의 섹션을 정의합니다.
+ ```<article>``` - 독립된 자기 완결형 콘텐츠를 정의합니다.
+ ```<aside>``` - 콘텐츠 이외의 콘텐츠를 정의합니다(사이드바 등).
+ ```<footer>``` - 문서 또는 섹션의 바닥글을 정의합니다.
+ ```<details>``` - 사용자가 필요에 따라 열고 닫을 수 있는 추가 세부 정보 정의
+ ```<summary>``` - ```<details>``` 요소의 제목을 정의합니다.

차후 시맨틱장에서 깊이 알아봅니다.

## HTML 레이아웃 기술

멀티 컬럼 레이아웃을 작성하는 방법에는 4가지가 있습니다. 각 기술에는 장단점이 있습니다.

+ CSS 프레임워크
+ CSS 플로트 속성
+ CSS 플렉스 박스
+ CSS 그리드

## CSS 프레임워크

레이아웃을 빠르게 작성하려면 W3.CSS 또는 부트스트랩 등의 CSS 프레임워크를 사용할 수 있습니다.

## CSS 플로트 레이아웃

일반적으로 CSS float 속성을 사용하여 전체 웹 레이아웃을 수행합니다. 플로트는 배우기 쉽습니다.플로트와 클리어 속성이 어떻게 작동하는지 기억하기만 하면 됩니다. 

단점: 플로팅 요소는 문서 흐름에 연결되어 있어 유연성이 저하될 수 있습니다. 플로트에 대한 자세한 내용은 CSS Float and Clear 장에서 깊이 알아봅니다.

## CSS 플렉스 레이아웃

플렉스 박스를 사용하면, 페이지 레이아웃이 다른 화면 사이즈와 다른 디스플레이 디바이스에 대응할 필요가 있는 경우에, 요소가 예측 가능하게 동작할 수 있습니다.

Flexbox에 대한 자세한 내용은 CSS Flexbox 장에서 깊이 알아봅니다.

## CSS 그리드 레이아웃

CSS 그리드 레이아웃 모듈은 행과 컬럼이 있는 그리드 기반 레이아웃 시스템을 제공하여 플로트나 포지셔닝 없이 웹 페이지를 쉽게 설계할 수 있습니다.

CSS 그리드에 대한 자세한 내용은 CSS grid 장에서 깊이 알아봅니다.
