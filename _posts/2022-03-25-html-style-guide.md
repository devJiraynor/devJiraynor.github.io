---
layout: post
title: HTML 28. 스타일 가이드 (Style Guide)
subtitle: HTML 코드가 일관되고 깔끔하며 정돈되어 있기 때문에 다른 사람이 코드를 쉽게 읽고 이해할 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 스타일 가이드

## 문서 유형 항상 선언

항상 문서 유형을 문서의 첫 번째에 선언하십시오.

HTML의 올바른 문서 유형은 다음과 같습니다.

```html
<!DOCTYPE html>
```

## 모든 요소 이름에 소문자 사용

HTML에서는 요소 이름에 대소문자를 혼합할 수 있습니다.

하지만, 다음과 같은 이유로 요소 이름은 소문자로 사용하는 것이 좋습니다.

+ 대소문자를 혼용하면 깔끔하지 않습니다.
+ 개발자는 일반적으로 소문자 이름을 사용합니다.
+ 소문자가 깔끔하게 표시됩니다.
+ 소문자가 쓰기 쉽다.

###### 예제 1 - good

```html
<body>
<p>This is a paragraph.</p>
</body>
```

###### 예제 1 - bad

```html
<BODY>
<P>This is a paragraph.</P>
</BODY>
```

## 모든 HTML 요소 닫기

HTML 에서는 모든 요소(```<p>``` 요소등)를 닫을 필요는 없습니다.

하지만, 모든 HTML 요소를 닫는 것이 좋습니다.

###### 예제 2 - good

```html
<section>
  <p>This is a paragraph.</p>
  <p>This is a paragraph.</p>
</section>
```

###### 예제 2 - bad

```html
<section>
  <p>This is a paragraph.
  <p>This is a paragraph.
</section>
```

## 모든 속성 이름에 소문자 사용

HTML에서는 속성 이름에 대소문자를 혼합할 수 있습니다.

하지만, 다음과 같은 이유로 요소 이름은 소문자로 사용하는 것이 좋습니다.

+ 대소문자를 혼용하면 깔끔하지 않습니다.
+ 개발자는 일반적으로 소문자 이름을 사용합니다.
+ 소문자가 깔끔하게 표시됩니다.
+ 소문자가 쓰기 쉽습니다.

###### 예제 3 - good

```html
<a href="https://www.w3schools.com/html/">Visit our HTML tutorial</a>
```

###### 예제 3 - bad

```html
<a HREF="https://www.w3schools.com/html/">Visit our HTML tutorial</a>
```

## 속성 값에 항상 따옴표 사용

HTML 에서는 따옴표 없이 속성 값을 사용할 수 있습니다.

하지만, 다음과 같은 이유로 속성 값에 따옴표를 사용하는 것이 좋습니다.

+ 개발자는 일반적으로 속성 값에 따옴표를 사용합니다.
+ 따옴표로 묶인 값을 더 쉽게 읽을 수 있습니다.
+ 값에 공백이 포함된 경우 따옴표를 사용해야 합니다.

###### 예제 4 - good

```html
<table class="striped">
```

###### 예제 5 - bad

```html
<table class=striped>
```

###### 예제 5 - very bad

```html
<table class=table striped>
```

## 이미지의 alt, width 및 height 항상 지정

이미지의 ```alt``` 속성을 항상 지정하십시오. 이 속성은 어떤 이유로 이미지를 표시할 수 없는 경우에 중요합니다.

또한 이미지의 ```width``` 와 ```height``` 를 항상 정의하십시오. 그러면 브라우저가 로드하기 전에 이미지 공간을 할당할 수 있으므로 로딩이 줄어듭니다.

###### 예제 6 - good

```html
<img src="html5.gif" alt="HTML5" style="width:128px;height:128px">
```

###### 예제 6 - bad

```html
<img src="html5.gif">
```

## 등호와 공백

HTML에서는 등호 주위에 공백을 둘 수 있습니다. 그러나 공백 제거는 읽기 쉽고 엔티티를 더 잘 그룹화합니다.

###### 예제 7 - good

```html
<link rel="stylesheet" href="styles.css">
```

###### 예제 7 - bad

```html
<link rel = "stylesheet" href = "styles.css">
```

## 긴 줄 코드를 피하세요

HTML 에디터를 사용할 때 HTML 코드를 읽기 위해 좌우로 스크롤하는 것은 편리하지 않습니다.

코드 행이 너무 길지 않도록 하십시오.

## 빈 줄과 들여쓰기

이유 없이 빈 줄, 공백 또는 들여쓰기를 추가하지 마십시오.

읽기 쉽도록 큰 코드 블록 또는 논리 코드 블록에 빈 행을 추가합니다.

읽기 쉽도록 들여쓰기 공간을 두 개 추가합니다. 탭 키를 사용하지 마십시오.

###### 예제 8 - good

```html
<body>

<h1>Famous Cities</h1>

<h2>Tokyo</h2>
<p>Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
and the most populous metropolitan area in the world.
It is the seat of the Japanese government and the Imperial Palace,
and the home of the Japanese Imperial Family.</p>

</body>
```

###### 예제 8 - bad

```html
<body>

  <h1>Famous Cities</h1>

  <h2>Tokyo</h2>

  <p>
    Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
    and the most populous metropolitan area in the world.
    It is the seat of the Japanese government and the Imperial Palace,
    and the home of the Japanese Imperial Family.
  </p>

</body>
```

###### 예제 8 - good table

```html
<table>
  <tr>
    <th>Name</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>A</td>
    <td>Description of A</td>
  </tr>
  <tr>
    <td>B</td>
    <td>Description of B</td>
  </tr>
</table>
```

###### 예제 8 - good list

```html
<ul>
  <li>London</li>
  <li>Paris</li>
  <li>Tokyo</li>
</ul>
```

## ```<title>``` 요소를 빼먹지 마세요

``` <title>``` 요소는 HTML에서 필요합니다.

검색엔진최적화(SEO)에는 페이지 제목 내용이 매우 중요합니다! 페이지 제목은 검색 결과에 페이지를 나열할 때 검색 엔진 알고리즘에서 순서를 결정하는 데 사용됩니다.

```<title>``` 요소는

+ 브라우저 툴바에 제목을 정의합니다.
+ 페이지를 즐겨찾기에 추가할 때 페이지 제목을 제공합니다.
+ 검색 엔진 결과 페이지 제목을 표시합니다.

따라서 가능한 한 정확하고 의미 있는 제목을 만드십시오.

###### 예제 9

```html
<title>HTML Style Guide and Coding Conventions</title>
```

## ```<html>``` 과 ```<body>``` 를 생략하시겠습니까?
  
HTML 페이지에서는 ```<html>``` 및 ```<body>``` 태그 없이도 가능합니다.

###### 예제 10

```html
<!DOCTYPE html>
<head>
  <title>Page Title</title>
</head>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>
```

하지만, ```<html>``` 태그와 ```<body>``` 태그를 항상 추가할 것을 강력히 권장합니다.

```<body>``` 를 생략하면 오래된 브라우저에서 오류가 발생할 수 있습니다.

```<html>``` 및 ```<body>``` 를 생략하면 DOM 및 XML 소프트웨어에서 오류가 발생 할 수 있습니다.

## ```<head>``` 를 생략하시겠습니까?

HTML ```<head>``` 태그도 생략할 수 있습니다.

브라우저는 기본 ```<head>``` 요소에 ```<body>``` 앞에 있는 모든 요소를 추가합니다.

###### 예제 11

```html
<!DOCTYPE html>
<html>
<title>Page Title</title>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```

하지만, ```<head>``` 태그를 사용할 것을 권장합니다.

## 빈 HTML 요소를 닫으시겠습니까?

HTML 에서는 빈 요소를 닫는 것은 옵션입니다.

###### 예제 12 - 빈 요소 닫지 않기 (가능)

```html
<meta charset="utf-8">
```

###### 예제 12 - 빈 요소 닫기 (가능)

```html
<meta charset="utf-8" />
```

XML/XHTML 소프트웨어가 페이지에 액세스 할 것으로 예상되는 경우는 XML 및 XHTML에 클로징 슬래시(/)를 필요로 합니다.

## lang 속성 추가

웹 페이지의 언어를 선언하려면 항상 ```<html>``` 태그 안에 ```lang``` 속성을 포함해야 합니다. 이것은 검색 엔진과 브라우저를 지원하기 위한 것입니다.
  
###### 예제 13

```html
<!DOCTYPE html>
<html lang="ko-kr">
<head>
  <title>Page Title</title>
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```

## 메타 데이터

올바른 해석과 올바른 검색 엔진 인덱싱을 위해 HTML 문서에서 언어와 문자 인코딩 ```<meta charset="charset">``` 을 가능한 한 앞에 정의해야 합니다.

###### 예제 14

```html
<!DOCTYPE html>
<html lang="en-us">
<head>
  <meta charset="UTF-8">
  <title>Page Title</title>
</head>
```

## 뷰포트 설정

뷰포트는 사용자가 웹 페이지에서 볼 수 있는 영역입니다. 단말기에 따라 다릅니다. 휴대전화에서는 컴퓨터 화면보다 작습니다.

모든 웹 페이지에 다음 ```<meta>``` 요소를 포함해야 합니다.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

그러면 브라우저에 페이지 치수와 축척를 제어하는 방법에 대한 지침이 제공됩니다.

```width=device-width``` 부분은 디바이스의 화면폭에 따르도록 페이지 폭을 설정합니다(단말기에 따라 다릅니다).

```initial-scale=1.0``` 부분은 브라우저에 의해 페이지가 처음 로드될 때의 초기 줌 레벨을 설정합니다.

## HTML 주석

짧은 주석은 한 줄에 다음과 같이 적습니다.

```html
<!-- 짧은 주석입니다. -->
```

여러 줄에 걸친 주석은 다음과 같이 작성해야 합니다.

```html
<!--
  두 줄에 걸친 긴 주석입니다.
  두 줄에 걸친 긴 주석입니다.
-->
```

긴 주석은 공백이 두 개 있는 경우 확인이 쉽습니다.

## 스타일 시트 사용

스타일 시트에 연결하려면 간단한 구문을 사용합니다(```type``` 속성은 필요하지 않음).

```html
<link rel="stylesheet" href="styles.css">
```

짧은 CSS 규칙은 다음과 같이 압축하여 쓸 수 있습니다.

```css
p.intro {font-family:Verdana;font-size:16em;}
```

긴 CSS 규칙은 여러 줄에 걸쳐 작성해야 합니다.

```css
body {
  background-color: lightgrey;
  font-family: "Arial Black", Helvetica, sans-serif;
  font-size: 16em;
  color: black;
}
```

+ 시작 중괄호를 (```{```) 셀렉터와 같은 라인에 놓습니다.
+ 시작 중괄호 앞에 공백을 하나 사용합니다.
+ 두 개의 들여쓰기 공간 사용합니다.
+ 각 속성-값 쌍 뒤에 세미콜론 사용합니다.(마지막 포함)
+ 값에 공백이 포함된 경우에만 값 주위에 따옴표를 사용하십시오.
+ 선두 공백 없이 새 줄에 닫는 중괄호를 배치합니다.

## HTML에서 JavaScript 로드

외부 스크립트를 로드하려면 간단한 구문을 사용합니다(```type``` 속성은 필요하지 않습니다).

```html
<script src="myscript.js">
```

## JavaScript를 사용한HTML 요소 접근

"정돈되지 않은" HTML 코드를 사용하면 JavaScript 오류가 발생할 수 있습니다.

이 두 개의 JavaScript 문장은 다른 결과를 생성합니다.

###### 예제 15

```javascript
getElementById("Demo").innerHTML = "Hello";

getElementById("demo").innerHTML = "Hello";
```

## 소문자 파일 이름 사용

일부 웹 서버(Apache, Unix)는 파일 이름에 대해 대소문자를 구분합니다. "london.jpg"는 "London.jpg"로 액세스할 수 없습니다.

기타 웹 서버(Microsoft, IIS)에서는 대소문자가 구분되지 않습니다.「 london . jpg 」는 「London . jpg 」로서 액세스 할 수 있습니다.

대문자와 소문자를 혼용하는 경우, 이 점에 주의해 주세요.

대소문자를 구분하지 않는 서버에서 대소문자를 구분하는 서버로 이행하면 사소한 오류에도 웹이 손상됩니다.

이러한 문제를 방지하려면 항상 소문자 파일 이름을 사용하십시오.

## 파일 확장자

HTML 파일의 확장자는 **.html**이어야 합니다 **.htm**은 허용됩니다.

CSS 파일의 확장자는 **.css**이어야 합니다.

JavaScript 파일의 확장자는 **.js**이어야 합니다.

## .htm과 .html의 차이점

.htm 파일 확장자와 .html 파일 확장자는 차이가 없습니다.

어느 웹 브라우저 및 웹 서버에서도 둘 다 HTML로 취급됩니다.

## 기본 파일 이름

URL 끝에 파일 이름이 지정되지 않은 경우(예: "https://github.com/"), "index.htm", "default.htm" 또는 "default.htm"과 같은 기본 파일 이름이 추가됩니다.

서버가 기본 파일명으로 "index.html"로만 구성되어 있는 경우 파일 이름은 "default.html"이 아니라 "index.html"이어야 합니다.

다만, 서버는 복수의 디폴트 파일명으로 설정할 수 있습니다. 통상은, 디폴트 파일명을 필요한 수만큼 설정할 수 있습니다.

