---
layout: post
title: HTML 12. 링크 (Links)
subtitle: 링크는 거의 모든 웹 페이지에 있습니다. 링크를 통해 사용자는 페이지 간에 자신의 길을 클릭할 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/lsrJOHi4JmE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<a href="https://youtu.be/lsrJOHi4JmE" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 12. 링크 (Links)</a>
<br>
<br>

# HTML 링크

## HTML 링크 - 하이퍼링크

HTML 링크는 하이퍼링크입니다.

링크를 누른 후 다른 문서로 이동할 수 있습니다.

마우스를 링크 위로 이동하면 마우스 화살표가 작은 손으로 바뀝니다.

{: .box-note}
**Note:** 링크가 텍스트일 필요는 없습니다. 링크는 이미지 또는 기타 HTML 요소가 될 수 있습니다.

## HTML 링크 - 구문

HTML ```<a>``` 태그는 하이퍼링크를 정의합니다. 구문은 다음과 같습니다.

```html
<a href="url">링크 텍스트</a>
```

```<a>``` 요소의 가장 중요한 속성은 링크의 수신처를 나타내는 ```href``` 속성입니다.

링크 텍스트는 독자가 볼 수 있는 부분입니다.

링크 텍스트를 클릭하면 리더가 지정된 URL 주소로 전송됩니다.

###### 예제 1

```html
<a href="https://devjiraynor.github.io/">Jiraynor`s blog</a>
```

기본적으로 링크는 모든 브라우저에 다음과 같이 표시됩니다.

+ 방문하지 않은 링크에 밑줄이 그어져 파란색으로 표시됩니다.
+ 방문한 링크는 밑줄이 그어져 보라색입니다.
+ 활성 링크에 밑줄이 그어져 빨간색으로 표시됩니다.

{: .box-note}
**Tip:** 링크는 CSS로 스타일링할 수 있어 다른 스타일로 표시할 수 있습니다.

## HTML 링크 - 타겟 속성

기본적으로 링크된 페이지는 현재 브라우저 창에 표시됩니다. 이를 변경하려면 링크에 다른 대상을 지정해야 합니다.

```target``` 속성은 연결된 문서를 열 위치를 지정합니다.

```target``` 속성에는, 다음의 값을 지정할 수 있습니다.

+ ```_self``` - 디폴트. 누른 것과 동일한 창/탭에서 문서를 엽니다.
+ ```_blank``` - 새 창 또는 탭에서 문서를 엽니다.
+ ```_parent``` - 상위 프레임에서 문서를 엽니다.
+ ```_top``` - 창 전체의 본문에서 문서를 엽니다.

###### 예제 2

```html
<a href="https://devjiraynor.github.io/" target="_blank">Jiraynor`s blog</a>
```

## 절대 경로 vs. 상대 경로

위의 두 예 모두 ```href``` 속성에 **절대 URL(풀 웹 주소)** 을 사용하고 있습니다.

로컬 링크(같은 웹 사이트 내의 페이지에 대한 링크)는 **상대 URL** 로 지정됩니다("https://www" 부분 없음).

###### 예제 3

```html
<h2>Absolute URLs</h2>
<p><a href="https://www.w3.org/">W3C</a></p>
<p><a href="https://www.google.com/">Google</a></p>

<h2>Relative URLs</h2>
<p><a href="html_images.asp">HTML Images</a></p>
<p><a href="/css/default.asp">CSS Tutorial</a></p>
```

## HTML 링크 - 이미지를 링크로 사용

이미지를 링크로 사용하려면 ```<a>``` 태그 안에 ```<img>``` 태그를 넣기만 하면 됩니다.

###### 예제 4

```html
<a href="default.asp">
<img src="smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;">
</a>
```

## 이메일 주소 링크

```href``` 속성 내에 ```mailto:``` 를 사용하여 사용자의 이메일 프로그램을 여는 링크를 만듭니다(새 이메일을 보낼 수 있도록 함).

###### 예제 5

```html
<a href="mailto:lacls159@gmail.com">메일 전송</a>
```

## 링크로서의 버튼

HTML 버튼을 링크로 사용하려면 JavaScript 코드를 추가해야 합니다.

JavaScript를 사용하면 버튼 클릭과 같은 특정 이벤트에서 발생하는 작업을 지정할 수 있습니다.

###### 예제 6

```html
<button onclick="document.location='default.asp'">HTML Tutorial</button>
```

## 링크 제목

```title``` 속성은 요소에 대한 추가 정보를 지정합니다. 대부분의 경우 마우스를 요소 위로 이동하면 정보가 툴팁 텍스트로 표시됩니다.

###### 예제 7

```html
<a href="https://devjiraynor.github.io/" title="Jiraynor`s blog">Visit Jiraynor`s blog</a>
```

## Summary

+ ```<a>``` 요소를 사용하여 링크를 정의합니다.
+ ```href``` 속성을 사용하여 링크주소를 정의합니다.
+ ```target``` 속성을 사용하여 연결된 문서를 열 위치를 정의합니다.
+ 이미지를 링크로 사용하려면 ```<img>``` 요소( ```<a>``` 내부)를 사용합니다.
+ ```href``` 속성 내의 ```mailto:``` 스키마를 사용하여 사용자의 이메일 프로그램을 여는 링크를 만듭니다.

# HTML 링크 - 다른 색상

## HTML 링크 색상

기본적으로 링크는 다음과 같이 표시됩니다.

+ 방문하지 않은 링크에 밑줄이 그어져 파란색으로 표시됩니다.
+ 방문한 링크는 밑줄이 그어져 보라색입니다.
+ 활성 링크에 밑줄이 그어져 빨간색으로 표시됩니다.

CSS를 사용하여 링크 상태 색상을 변경할 수 있습니다.

###### 예제 8

```html
<style>
a:link {
  color: green;
  background-color: transparent;
  text-decoration: none;
}

a:visited {
  color: pink;
  background-color: transparent;
  text-decoration: none;
}

a:hover {
  color: red;
  background-color: transparent;
  text-decoration: underline;
}

a:active {
  color: yellow;
  background-color: transparent;
  text-decoration: underline;
}
</style>
```

## 링크 버튼

CSS를 사용하여 링크는 버튼으로 스타일링할 수도 있습니다.

###### 예제 9

```html
<style>
a:link, a:visited {
  background-color: #f44336;
  color: white;
  padding: 15px 25px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
}

a:hover, a:active {
  background-color: red;
}
</style>
```

# HTML 링크 북마크 생성

## HTML로 북마크 작성

북마크는 웹 페이지가 매우 긴 경우 유용합니다.

북마크를 작성하려면 먼저 북마크를 작성한 후 북마크에 링크를 추가합니다.

링크를 클릭하면 페이지가 아래로 스크롤되거나 북마크가 있는 위치까지 스크롤됩니다.

###### 예제 10

먼저 ```id``` 속성을 사용하여 북마크를 만듭니다.

```html
<h2 id="C4">Chapter 4</h2>
```

그런 다음 같은 페이지 내에서 북마크("4장으로")에 링크를 추가합니다.

```html
<a href="#C4">4장으로</a>
```

다른 페이지의 책갈피에 링크를 추가할 수도 있습니다.

```html
<a href="html_demo.html#C4">4장으로</a>
```

