---
layout: post
title: HTML 34. HTML vs XHTML
subtitle: XHTML은 보다 엄격한 XML 기반의 HTML 버전입니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<a href="https://youtu.be/EN7o5g61wbA" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 34. HTML vs XHTML 영상 보러가기</a>
<br>
<br>

# HTML vs XHTML

## XHTML 이란?

+ XHTML은 E**X**tensible **H**yper**T**ext **M**arkup **L**anguage의 약자입니다.
+ XHTML은 보다 엄격한 XML 기반의 HTML 버전입니다.
+ XHTML은 XML 어플리케이션으로 정의되어 있습니다.
+ XHTML은 모든 주요 브라우저에서 지원됩니다.

## 왜 XHTML 을 사용하는가?

XML은 모든 문서를 올바르게 표시해야 하는 마크업 언어입니다 ('양식이 엄격합니다.')

XHTML은 HTML을 다른 데이터 형식(XML 등)과 함께 사용할 수 있도록 확장성과 유연성을 높이기 위해 개발되었습니다. 또한 브라우저는 HTML 페이지의 오류를 무시하고 마크업에 오류가 있더라도 웹 사이트를 표시하려고 합니다. 따라서 XHTML은 훨씬 더 엄격한 오류 처리를 제공합니다.

## HTML과의 가장 중요한 차이점

+ ```<!DOCTYPE>```은 **필수** 입니다.
+ ```<html>```의 ```xmlns``` 속성은 **필수**입니다.
+ ```<html>```, ```<head>```, ```<title>```, ```<body>```는 **필수**입니다.
+ 요소는 항상 **올바르게 중첩**되어야 합니다.
+ 요소는 항상 **닫아야** 합니다.
+ 요소는 항상 **소문자**여야 합니다.
+ 특성 이름은 항상 **소문자**여야 합니다.
+ 특성 값은 항상 **따옴표**로 묶어야 합니다.
+ 속성 최소화는 **금지**되어 있습니다.

## ```<!DOCTYPE>```은 필수

XHTML 문서에는 XHTML ```<!DOCTYPE>``` 선언은 반드시 필요합니다.

```<html>```, ```<head>```, ```<title>``` 및 ```<body>``` 요소도 존재해야 하며, ```<html>```의 ```xmlns``` 속성은 문서의 xml 네임스페이스를 지정해야 합니다.

###### 예시 1 - 최소 필수 태그를 가진 XHTML 문서

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN"
"http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
  <title>Title of document</title>
</head>
<body>

  some content here...

</body>
</html>
```

## XHTML 요소가 올바르게 중첩되어야 함

XHTML에서는 다음과 같이 요소가 항상 서로 적절하게 중첩되어야 합니다.

###### 예시 2 - correct

```html
<b><i>Some text</i></b>
```

###### 예시 2 - wrong

```html
<b><i>Some text</b></i>
```

## XHTML 요소는 항상 닫아야 합니다.

XHTML에서는 다음과 같이 요소를 항상 닫아야 합니다.

###### 예시 3 - correct

```html
<p>This is a paragraph</p>
<p>This is another paragraph</p>
```

###### 예시 3 - wrong

```html
<p>This is a paragraph
<p>This is another paragraph
```

## XHTML 빈 요소는 항상 닫아야 합니다.

XHTML에서는 다음과 같이 빈 요소는 항상 닫아야 합니다.

###### 예시 4 - correct

```html
A break: <br />
A horizontal rule: <hr />
An image: <img src="happy.gif" alt="Happy face" />
```

###### 예시 4 - wrong

```html
A break: <br>
A horizontal rule: <hr>
An image: <img src="happy.gif" alt="Happy face">
```

## XHTML 요소는 소문자여야 합니다.

XHTML 에서는 요소명은 항상 다음과 같이 소문자로 할 필요가 있습니다.

###### 예시 5 - correct

```html
<body>
<p>This is a paragraph</p>
</body>
```

###### 예시 5 - wrong

```html
<BODY>
<P>This is a paragraph</P>
</BODY>
```

## XHTML 속성 이름은 소문자로 입력해야 합니다.

XHTML에서는 속성 이름은 항상 다음과 같이 소문자로 할 필요가 있습니다.

###### 예시 6 - correct

```html
<a href="https://devjiraynor.github.io/">Jiraynor blog</a>
```

###### 예시 6 - wrong

```html
<a HREF="https://devjiraynor.github.io/">Jiraynor blog</a>
```

## XHTML 속성 값은 따옴표로 묶어야 합니다.

XHTML에서는 속성 값은 항상 다음과 같이 따옴표로 묶어야 합니다.

###### 예시 7 - correct

```html
<a href="https://devjiraynor.github.io/">Jiraynor blog</a>
```

###### 예시 7 - wrong

```html
<a HREF=https://devjiraynor.github.io/>Jiraynor blog</a>
```

## XHTML 속성 최소화는 금지되어 있습니다.

XHTML에서는 속성 최소화는 금지되어 있습니다.

###### 예시 8 - correct

```html
<input type="checkbox" name="vehicle" value="car" checked="checked" />
<input type="text" name="lastname" disabled="disabled" />
```

###### 예시 8 - wrong

```html
<input type="checkbox" name="vehicle" value="car" checked />
<input type="text" name="lastname" disabled />
```

## W3C Validator를 사용한 HTML 검증

아래 상자에 웹 주소를 입력하십시오.

<form method="GET" action="https://validator.w3.org/check">
  <input name="uri" size="60" value="https://www.naver.com/" style="max-width: 100%" />
  <input type="submit" value="페이지 검증" />
</form>
