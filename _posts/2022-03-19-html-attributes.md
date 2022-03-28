---
layout: post
title: HTML 03. 속성 (Attributes)
subtitle: HTML 속성은 HTML 요소에 대한 추가 정보를 제공합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/ruMsX197V5s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<a href="https://youtu.be/ruMsX197V5s" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 03. 속성 (Attributes)</a>
<br>
<br>


# HTML 속성(Attributes)   
   
   
## HTML 속성   
   
+ 모든 HTML 요소는 속성을 가질 수 있습니다.   
+ 속성은 요소에 대한 추가 정보를 제공합니다.   
+ 속성은 항상 시작 태그에 지정됩니다.   
+ 속성은 일반적으로 name="value"와 같은 이름/값 쌍으로 제공됩니다.   
   
## href 속성   
   
```<a>``` 태그는 하이퍼링크를 정의합니다. ```href``` 속성은 링크가 다음 페이지로 이동하는 URL을 지정합니다.
   
###### 예제 1   
   
```html
<a href="https://devjiraynor.github.io/">Jiraynor github 블로그</a>
```   
   
## src 속성   
   
```<img>``` 태그는 이미지를 HTML 페이지에 삽입하기 위해 사용됩니다. ```src``` 속성은 표시할 이미지에 대한 경로를 지정합니다.
   
###### 예제 2   
   
```html
<img src="html_thumb.png">
```   
   
```src``` 속성으로 URL을 지정하는 방법에는 다음 두 가지가 있습니다.   
   
**1. 절대 경로 -** 다른 웹 사이트에서 호스트되는 외부 이미지에 대한 링크, 완전한 URL 주소   
예: https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html_thumb.png   
   
{: .box-warning}
**Warning:** 외부 이미지는 저작권에 속할 수 있습니다. 사용허가를 받지 못할 경우 저작권법 위반이 될 수 있습니다. 또한 외부 이미지는 제어할 수 없습니다. 갑자기 제거되거나 변경될 수 있습니다.   
   
**2. 상대 경로 -** 웹 사이트 내에서 호스트되는 이미지에 대한 링크입니다. 여기서 URL은 도메인 이름을 포함하지 않습니다. 슬래시 없이 시작하는 URL은 현재 페이지를 기준으로 합니다.   
예: /assets/img/html_thumb.png   
   
{: .box-note}
**Tip:** 대부분의 경우 상대 URL을 사용하는 것이 가장 좋습니다. 도메인을 변경해도 끊어지지 않습니다.   
   
## width와 height 속성   
   
```<img>``` 태그에는 이미지의 폭과 높이(픽셀 단위)를 지정하는 ```width``` 와 ```height``` 속성도 포함되어 있어야 합니다.   
   
###### 예제 3   
   
```html
<img src="html_thumb.png" width="300" height="300">
```   
   
## alt 속성   
   
```<img>``` 태그의 필수 ```alt``` 속성은 어떤 이유로 이미지를 표시할 수 없는 경우 이미지의 대체 텍스트를 지정합니다. 이는 접속이 느리거나 ```src``` 속성에 오류가 있거나 사용자가 스크린 리더를 사용하는 경우에 발생할 수 있습니다.   
   
###### 예제 4   
   
```html
<img src="html_thumb.png" alt="html 썸네일">
```   
```html
<img src="html_thumb.jpg" alt="html 썸네일">
```   
   
## style 속성   
   
```style``` 속성은 색상, 글꼴, 크기 등과 같은 스타일을 요소에 추가하는 데 사용됩니다.   
   
###### 예제 5   

```html
<p style="color:red;">빨간색 문단</p>
```   
   
## lang 속성   
   
웹 페이지의 언어를 선언하려면 항상 ```<html>``` 태그 안에 ```lang``` 속성을 포함해야 합니다. 이것은 검색 엔진과 브라우저를 지원하기 위한 것입니다.   

다음 예제에서는 언어를 한글로 지정합니다.   
   
```html
<!DOCTYPE html>
<html lang="ko">
<body>
...
</body>
</html>
```   
   
국가 코드를 ```lang``` 속성의 언어 코드에 추가할 수도 있습니다. 따라서 처음 두 문자는 HTML 페이지의 언어를 정의하고 마지막 두 문자는 국가를 정의합니다.   
   
다음 예제에서는 언어를 한글로, 국가를 대한민국으로 지정하고 있습니다.   

```html
<!DOCTYPE html>
<html lang="ko-KR">
<body>
...
</body>
</html>
```   
   
## title 속성   
   
```title``` 속성은 요소에 대한 추가 정보를 정의합니다.   
   
title 속성 값은 요소 위에 마우스를 놓으면 도구 설명으로 표시됩니다.   
   
###### 예제 6   
   
```html
<p title="도구 설명">문단입니다.</p>
```   
   
## 권장 사항: 항상 소문자 속성 사용   
   
HTML 표준에서는 소문자 속성명이 필요하지 않습니다.   
   
제목 속성(및 기타 모든 속성)은 ```title``` 또는 ```TITLE``` 과 같이 대소문자를 사용하여 쓸 수 있습니다.   
   
하지만 HTML에서 소문자 속성을 **권장**하며 XHTML과 같은 더 엄격한 문서 유형에는 소문자 속성을 **요구**합니다.   
   
## 권장 사항: 속성 값은 항상 따옴표 사용   
   
HTML 표준에서는 속성 값 주위에 따옴표가 필요하지 않습니다.   
   
그러나 HTML로 따옴표를 사용하는 것을 **권장**하며 XHTML과 같은 더 엄격한 문서 유형에 대한 따옴표 사용을 **요구**합니다.   
   
###### 좋은 예   
   
```html
<a href="https://devjiraynor.github.io/">Jiraynor github 블로그</a>
```   
   
###### 나쁜 예   
   
```html
<a href=https://devjiraynor.github.io/>Jiraynor github 블로그</a>
```   
   
가끔은 따옴표를 사용해야 합니다. 다음 예에서는 공백이 포함되어 있기 때문에 제목 속성이 올바르게 표시되지 않습니다.   
   
```html
<p title=About HTML5>
```   
   
## 작은따옴표? 큰따옴표?   
   
HTML에서는 속성값 주위에 큰따옴표를 붙이는 것이 가장 일반적이지만 작은따옴표를 사용할 수도 있습니다.   
   
속성 값 자체에 큰따옴표가 포함되어 있는 경우 다음과 같이 작은따옴표를 사용해야 합니다.   
   
```html
<p title='"서지훈" jiraynor'>
<p title="'서지훈' jiraynor">
```   
   
## Summary   
   
+ 모든 HTML 요소는 **속성**을 가질 수 있습니다.   
+ ```<a>``` 의 ```href``` 속성은 링크의 이동할 페이지의 URL을 지정합니다.   
+ ```<img>``` 의 ```src``` 속성은 표시할 이미지의 경로를 지정합니다.   
+ ```<img>``` 의 ```width``` 와 ```height``` 속성은 이미지의 크기 정보를 제공합니다.   
+ ```<img>```의 ```alt``` 속성은 이미지의 대체 텍스트를 제공합니다.   
+ ```style``` 속성은 색상, 글꼴, 크기 등과 같은 스타일을 요소에 추가하는 데 사용됩니다.   
+ ```<html>``` 태그의 ```lang``` 속성은 웹 페이지의 언어를 선언합니다.   
+ ```title``` 속성은 요소에 대한 몇 가지 추가 정보를 정의합니다.   
   
