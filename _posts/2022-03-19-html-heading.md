---
layout: post
title: HTML 04. 헤딩 (Heading)
subtitle: HTML 헤딩(Heading) 웹 페이지에 표시할 제목 또는 자막입니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/IMI2Bb_SjIU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<a href="https://youtu.be/IMI2Bb_SjIU" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 04. 헤딩 (Heading)</a>
<br>
<br>

# HTML 헤딩   
   
      
## HTML 헤딩   
   
HTML 헤딩은 ```<h1>``` ~ ```<h6>``` 태그로 정의됩니다.

```<h1>``` 은 가장 중요한 제목을 정의합니다.   
```<h6>``` 는 가장 중요하지 않은 제목을 정의합니다.   
   
###### 예제 1   
   
```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```   
   
{: .box-note}
**Note:** 브라우저는 제목 앞뒤에 공백(여백)을 자동으로 추가합니다.   
   
## 헤딩은 중요합니다.   
   
검색 엔진은 헤딩을 사용하여 웹 페이지의 구조와 내용을 인덱싱합니다.   
   
사용자들은 종종 페이지의 헤딩을 훑어봅니다. 문서 구조를 표시하려면 헤딩을 사용하는 것이 중요합니다.   
   
주요 제목에는 ```<h1>``` 헤딩을 사용하고, 그 다음에 ```<h2>``` 헤딩을 사용하고, 다음으로 덜 중요한 ```<h3>``` 헤딩을 사용해야 합니다.   

   
{: .box-warning}
**Warning:** HTML 헤딩은 표제에만 사용합니다. 텍스트를 크게 하거나 굵게 하기 위해 제목을 사용하지 마십시오.    
   
## 큰 헤딩   
   
각 HTML 제목에는 기본 크기가 있습니다. 단, CSS ```font-size``` 속성을 사용하여 ```style``` 속성으로 임의의 헤더의 크기를 지정할 수 있습니다.   
   
###### 예제 2   
   
```html
<h1 style="font-size:60px;">Heading 1</h1>
```   
   
   
