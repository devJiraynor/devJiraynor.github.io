---
layout: post
title: HTML 09. 주석 (Comments)
subtitle: HTML 주석(Comments)은 브라우저에 표시되지 않지만 HTML 소스 코드를 문서화하는 데 도움이 됩니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<a href="https://youtu.be/cz87k4scewQ" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 09. 주석 (Comments) 영상 보러가기</a>
<br>
<br>

# HTML 주석

## HTML 주석 태그

다음 구문을 사용하여 HTML 소스에 주석을 추가할 수 있습니다.

```html
<!-- 여기에 코멘트를 써 주세요. -->
```

시작 태그에는 느낌표(!)가 있지만 끝 태그에는 없습니다.

{: .box-note}
**Note:** 주석은 브라우저에 표시되지 않지만 HTML 소스 코드를 문서화하는 데 도움이 됩니다.

## 주석 추가

주석을 사용하면, HTML 코드에 정보나 주의사항을 넣을 수 있습니다.

###### 예제 1

```html
<!-- 주석입니다. -->

<p>문단입니다.</p>

<!-- 여기에 정보를 추가하는 것을 잊지 마세요. -->
```

## 컨텐츠 숨기기

주석을 사용하여 컨텐츠를 숨길 수 있습니다.

컨텐츠를 일시적으로 숨길 경우 유용합니다.

###### 예제 2

```html
<p>첫번째 문단입니다.</p>

<!-- <p>추가한 문단입니다. </p> -->

<p>다른 문단입니다.</p>
```

또, 복수의 행을 숨길 수도 있습니다. ```<!--``` 와 ```-->``` 사이의 모든 행은 화면으로부터 숨겨집니다.

###### 예제 3

```html
<p>문단입니다.</p>
<!--
<p>이 멋진 이미지를 보세요.</p>
<img border="0" src="pic_trulli.jpg" alt="Trulli">
-->
<p>문단입니다.</p>
```

HTML 코드 행을 하나씩 코멘트 아웃하여 오류를 검색할 수 있기 때문에 HTML 디버깅에도 매우 적합합니다.

## 인라인 콘텐츠 숨기기

주석을 사용하여 HTML 코드 중간에 있는 부분을 숨길 수 있습니다.

###### 예제 4

```html
<p>안녕하세요! <!-- 날씨 -->좋은 아침입니다!</p>
```
