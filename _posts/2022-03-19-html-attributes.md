---
layout: post
title: HTML 3.속성(Attributes)
subtitle: HTML 속성은 HTML 요소에 대한 추가 정보를 제공합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 속성(Attributes)   
   
   
## HTML 속성   
   
+ 모든 HTML 요소는 속성을 가질 수 있습니다.   
+ 속성은 요소에 대한 추가 정보를 제공합니다.   
+ 속성은 항상 시작 태그에 지정됩니다.   
+ 속성은 일반적으로 name="value"와 같은 이름/값 쌍으로 제공됩니다.   
   
## href 속성   
   
```<a>``` 태그는 하이퍼링크를 정의합니다. ```href``` 속성은 링크가 다음 페이지로 이동하는 URL을 지정합니다.
   
###### 예제1   
   
```html
<a href="https://devjiraynor.github.io/">Jiraynor github 블로그</a>
```   
   
## src 속성   
   
```<img>``` 태그는 이미지를 HTML 페이지에 삽입하기 위해 사용됩니다. ```src``` 속성은 표시할 이미지에 대한 경로를 지정합니다.
   
###### 예제2   
   
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
   
###### 예제3   
   
```html
<img src="html_thumb.png" width="300" height="300">
```   
   
## alt 속성   
   
```<img>``` 태그의 필수 ```alt``` 속성은 어떤 이유로 이미지를 표시할 수 없는 경우 이미지의 대체 텍스트를 지정합니다. 이는 접속이 느리거나 ```src``` 속성에 오류가 있거나 사용자가 화면 리더를 사용하는 경우에 발생할 수 있습니다.   
   
###### 예제4   
   
```html
<img src="html_thumb.png" alt="html 섬네일">
```   
```html
<img src="html_thumb.jpg" alt="html 섬네일">
```   
   
