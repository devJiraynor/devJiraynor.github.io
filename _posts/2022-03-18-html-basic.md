---
layout: post
title: HTML 1.기본
subtitle: 이 장에서는 기본적인 HTML의 예를 몇 가지 소개합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 기본 예제   
   
   
## HTML 문서   
   
모든 HTML 문서는 문서 유형 선언( ```<!DOCTYPE html>``` )으로 시작해야 합니다.    
    
HTML 문서 자체는 ```<html>``` 로 시작하여 ```</html>``` 로 끝납니다.

HTML 문서의 표시 부분은 ```<body>``` 와 ```</body>``` 사이입니다.
   
###### 예제 1   
```html
<!DOCTYPE html>
<html>
<body>

<h1>글머리입니다.</h1>
<p>문단입니다.</p>

</body>
</html>
```
   
## <!DOCTYPE> 선언   
   
```<!DOCTYPE>``` 선언은 문서 유형을 나타내며 브라우저가 웹 페이지를 올바르게 표시할 수 있도록 도와줍니다.   
   
페이지 맨 위(HTML 태그 앞)에 한 번만 표시되어야 합니다.   
   
```<!DOCTYPE>``` 선언은 대소문자를 구분하지 않습니다.   
   
HTML5에 대한 ```<!DOCTYPE>``` 선언은 다음과 같습니다.   
   
###### 예제 2   
```html
<!DOCTYPE html>
```   
   
## HTML 글머리   
   
HTML 헤더는 ```<h1>``` ~ ```<h6>``` 태그로 정의됩니다.   
   
```<h1>``` 은 가장 중요한 제목을 정의합니다.   
```<h6>``` 는 가장 중요하지 않은 제목을 정의합니다.   
   
###### 예제 3   
```html
<h1>글머리 1</h1>
<h2>글머리 2</h2>
<h3>글머리 3</h3>
```   
   
## HTML 문단   
   
HTML 문단은 ```<p>``` 태그로 정의됩니다.
   
###### 예제 4    
```html
<p>첫번째 문단입니다.</p>
<p>다른 문단입니다.</p>
```   
   
## HTML 링크   
   
HTML 링크는 ```<a>``` 태그로 정의됩니다.   
   
###### 예제 5
```html
<a href="https://devJiraynor.github.io">이것은 링크입니다.</a>
```   
   
링크의 수신처는 ```href``` 속성으로 지정됩니다.   
   
## HTML 이미지   
   
HTML 이미지는 ```<img>``` 태그로 정의됩니다.

소스 파일( ```src``` ), 대체 텍스트( ```alt``` ), ```width``` 및 ```height``` 가 속성으로 제공됩니다.   
   
###### 예제 6   
```html
<img src="w3schools.jpg" alt="W3Schools.com" width="104" height="142">
```   
