---
layout: post
title: HTML 21. 자바스크립트 (Javascript)
subtitle: JavaScript는 HTML 페이지를 보다 동적이고 인터랙티브하게 만듭니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 자바스크립트

## HTML ```<script>``` 태그

HTML ```<script>``` 태그는 클라이언트측 스크립트(JavaScript)를 정의하기 위해 사용됩니다.

```<script>``` 요소에는 스크립트 문이 포함되거나 ```src``` 속성을 통해 외부 스크립트파일을 가리킵니다.

JavaScript의 일반적인 용도는 이미지 조작, 폼 검증 및 콘텐츠의 동적 변경입니다.

HTML 요소를 선택하기 위해 JavaScript는 ```document.getElementById()``` 메서드를 가장 많이 사용합니다.

다음 JavaScript 예제에서는 "Hello JavaScript!"를 id="http"인 HTML 요소에 씁니다.

###### 예제 1

```html
<script>
document.getElementById("demo").innerHTML = "Hello JavaScript!";
</script>
```

## JavaScript의 맛보기

다음은 JavaScript가 수행할 수 있는 몇 가지 예입니다.

###### 예제 2 - JavaScript는 내용을 변경할 수 있습니다.

```html
document.getElementById("demo").innerHTML = "Hello JavaScript!";
```

###### 예제 2 - JavaScript는 스타일을 변경할 수 있습니다.

```html
document.getElementById("demo").style.fontSize = "25px";
document.getElementById("demo").style.color = "red";
document.getElementById("demo").style.backgroundColor = "yellow";
```

###### 예제 2 - JavaScript는 속성을 변경할 수 있습니다.

```html
document.getElementById("image").src = "picture.gif";
```

## HTML ```<noscript>``` 태그
  
HTML ```<noscript>``` 태그는 브라우저에서 스크립트를 비활성화한 사용자 또는 스크립트를 지원하지 않는 브라우저를 가진 사용자에게 표시되는 대체 콘텐츠를 정의합니다.

###### 예제 3

```html
<script>
document.getElementById("demo").innerHTML = "Hello JavaScript!";
</script>
<noscript>Sorry, your browser does not support JavaScript!</noscript>
```
