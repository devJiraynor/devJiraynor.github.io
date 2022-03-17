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
*****   
   
## HTML 문서   
   
모든 HTML 문서는 문서 유형 선언( **<!DOCTYPE html>** )으로 시작해야 합니다.    
    
HTML 문서 자체는 **<html>** 로 시작하여 **</html>** 로 끝납니다.

HTML 문서의 표시 부분은 **<body>** 와 **</body>** 사이입니다.
   
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
   
     
##    
## <!DOCTYPE> 선언   
   
**<!DOCTYPE>** 선언은 문서 유형을 나타내며 브라우저가 웹 페이지를 올바르게 표시할 수 있도록 도와줍니다.   
   
페이지 맨 위(HTML 태그 앞)에 한 번만 표시되어야 합니다.   
   
**<!DOCTYPE>** 선언은 대소문자를 구분하지 않습니다.   
   
HTML5에 대한 **<!DOCTYPE>** 선언은 다음과 같습니다.   
   
```html
<!DOCTYPE html>
```   
   
