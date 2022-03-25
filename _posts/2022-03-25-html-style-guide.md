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
