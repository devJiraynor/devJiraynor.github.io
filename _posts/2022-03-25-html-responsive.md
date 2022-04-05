---
layout: post
title: HTML 25. 반응형 웹 디자인 (Responsive Web Design)
subtitle: 반응형 웹 디자인은 화면 크기와 뷰포트에 따라 자동으로 조정됩니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<a href="https://youtu.be/KwSlIXuvJhk" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 25. 반응형 웹 디자인 (Responsive Web Design) 영상 보러가기</a>
<br>
<br>

# HTML 반응형 웹 디자인

## 반응형 웹 디자인이란?

반응형 웹 디자인은 HTML과 CSS를 사용하여 모든 디바이스(데스크탑, 태블릿, 전화기)에서 보기 좋게 웹 사이트를 자동으로 크기 조정, 숨기기, 축소 또는 확대하는 것을 말합니다.

## 뷰포트 설정

반응형 웹 사이트를 작성하려면 , 다음의 ```<meta>``` 태그를 ```<head>``` 에 추가합니다.

###### 예제 1

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

그러면 페이지 뷰포트가 설정되고 브라우저에 페이지 치수와 축척을 제어하는 방법에 대한 지침이 나타납니다.

## 반응형 이미지

반응형 이미지는 브라우저 크기에 따라 적절하게 확장 가능한 이미지입니다.

###### ```width``` 속성 사용

```html
<img src="img_girl.jpg" style="width:100%;">
```

위의 예에서는 이미지를 원래 크기보다 크게 스케일업할 수 있습니다. 대부분의 경우 ```max-width``` 속성을 대신 사용하는 것이 좋습니다.

###### ```max-width``` 속성 사용

```html
<img src="img_girl.jpg" style="max-width:100%;height:auto;">
```

## 브라우저 폭에 따라 다른 이미지 표시

HTML ```<picture>``` 요소를 사용하면 브라우저 창 크기에 따라 다른 이미지를 정의할 수 있습니다.

###### 예제 2

```html
<picture>
  <source srcset="img_smallflower.jpg" media="(max-width: 600px)">
  <source srcset="img_flowers.jpg" media="(max-width: 1500px)">
  <source srcset="flowers.jpg">
  <img src="img_smallflower.jpg" alt="Flowers">
</picture>
```

## 반응형 텍스트 사이즈

텍스트 크기는 "vw" 단위로 설정할 수 있습니다. 즉, "viewport width(뷰포트 너비)"를 의미합니다.

###### 예제 3

```html
<h1 style="font-size:10vw">Hello World</h1>
```

{: .box-note}
뷰포트는 브라우저 창 크기입니다. 1vw = 뷰포트 폭의 1%. 뷰포트의 폭이 50cm일 경우 1vw는 0.5cm입니다.

## 미디어 쿼리

텍스트 및 이미지 크기 조정 외에도 반응형 웹 페이지에서 미디어 쿼리를 사용하는 것이 일반적입니다.

미디어 쿼리를 사용하면 브라우저 크기에 따라 완전히 다른 스타일을 정의할 수 있습니다.

###### 예제 4

```html
<style>
.left, .right {
  float: left;
  width: 20%; /* 폭은 기본적으로 20%입니다. */
}

.main {
  float: left;
  width: 60%; /* 폭은 기본적으로 60%입니다. */
}

/* 미디어 쿼리를 사용하여 800px에 중단점을 추가합니다. */
@media screen and (max-width: 800px) {
  .left, .main, .right {
    width: 100%; /* 뷰포트가 800px 이하일 경우 폭은 100%입니다. */
  }
}
</style>
```

## 반응형 웹 디자인 - 프레임워크

일반적인 CSS 프레임워크는 모두 응답성이 뛰어난 설계를 제공합니다.

대부분 무료이고 사용하기 쉽습다.

#### W3.CSS

W3.CSS는 데스크톱, 태블릿 및 모바일 설계를 기본적으로 지원하는 최신 CSS 프레임워크입니다.

W3.CSS는 유사한 CSS 프레임워크보다 작고 빠릅니다.

W3.CSS는 부트스트랩의 고품질 대체품이 되도록 설계되어 있습니다.

W3.CSS는 jQuery 또는 기타 JavaScript 라이브러리에서 독립적으로 설계되었습니다.

###### 예제 5

```html
<!DOCTYPE html>
<html>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
<body>

<div class="w3-container w3-green">
  <h1>W3Schools Demo</h1>
  <p>Resize this responsive page!</p>
</div>

<div class="w3-row-padding">
  <div class="w3-third">
    <h2>London</h2>
    <p>London is the capital city of England.</p>
    <p>It is the most populous city in the United Kingdom,
    with a metropolitan area of over 13 million inhabitants.</p>
  </div>

  <div class="w3-third">
    <h2>Paris</h2>
    <p>Paris is the capital of France.</p>
    <p>The Paris area is one of the largest population centers in Europe,
    with more than 12 million inhabitants.</p>
  </div>

  <div class="w3-third">
    <h2>Tokyo</h2>
    <p>Tokyo is the capital of Japan.</p>
    <p>It is the center of the Greater Tokyo Area,
    and the most populous metropolitan area in the world.</p>
  </div>
</div>

</body>
</html>
```

#### Bootstrap

또 하나의 일반적인 CSS 프레임워크는 부트스트랩입니다. 부트스트랩은 HTML, CSS 및 jQuery를 사용하여 응답성이 높은 웹 페이지를 만듭니다.

```html
<!DOCTYPE html>
<html lang="en">
<head>
<title>Bootstrap Example</title>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script>
</head>
<body>

<div class="container">
  <div class="jumbotron">
    <h1>My First Bootstrap Page</h1>
  </div>
  <div class="row">
    <div class="col-sm-4">
      ...
    </div>
    <div class="col-sm-4">
      ...
    </div>
    <div class="col-sm-4">
    ...
    </div>
  </div>
</div>

</body>
</html>
```
