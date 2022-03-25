---
layout: post
title: HTML 31. 이모지 (Emojis)
subtitle: 이모티콘은 UTF-8 문자 집합의 문자입니다. 😄😍💗
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 이모지

## 이모지란?

이모지는 이미지나 아이콘처럼 보이지만 그렇지 않습니다.

UTF-8(Unicode) 문자 세트의 문자(문자)입니다.

{: .box-note}
UTF-8은 전 세계의 거의 모든 문자와 기호를 포함합니다.

## HTML 문자셋 속성

HTML 페이지를 올바르게 표시하려면 웹 브라우저가 페이지에서 사용되는 문자 집합을 알아야 합니다.

이것은 ```<meta>``` 태그에 지정되어 있습니다.

```html
<meta charset="UTF-8">
```

{: .box-note}
지정하지 않으면 UTF-8이 HTML 기본 문자 집합입니다.

## UTF-8 문자셋

UTF-8 문자는 키보드로 입력할 수 없지만 항상 숫자(엔티티 번호)를 사용하여 표시할 수 있습니다.

+ A : 65
+ B : 66
+ C : 67

###### 예제 1

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
</head>
<body>

<p>I will display A B C</p>
<p>I will display &#65; &#66; &#67;</p>

</body>
</html>
```

###### 예제 설명

```<meta charset="UTF-8">``` 요소는 문자 세트를 정의합니다.

문자 A, B 및 C는 65, 66 및 67의 숫자로 표시됩니다.

브라우저가 문자를 표시하고 있음을 인식시키려면 엔티티 번호를 ```&#```으로 시작하고 엔티티 번호를 ;(세미콜론)으로 끝내야 합니다.

## 이모지 문자

이모지는 UTF-8 알파벳 문자이기도 합니다.

+ 😄 is 128516
+ 😍 is 128525
+ 💗 is 128151

###### 예제 2

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
</head>
<body>

<h1>My First Emoji</h1>

<p>&#128512;</p>

</body>
</html>
```

이모지는 문자이므로 HTML의 다른 문자처럼 복사, 표시 및 크기를 지정할 수 있습니다.

###### 예제 3

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
</head>
<body>

<h1>Sized Emojis</h1>

<p style="font-size:48px">
&#128512; &#128516; &#128525; &#128151;
</p>

</body>
</html>
```

## UTF-8의 일부 이모티콘 기호

| 이모지 | 이모지번호 |
| &#128507; | ```&#128507;``` |
| &#128508; | ```&#128508;``` |
| &#128509; | ```&#128509;``` |
| &#128510; | ```&#128510;``` |
| &#128511; | ```&#128511;``` |
| &#128512; | ```&#128512;``` |
| &#128513; | ```&#128513;``` |
| &#128514; | ```&#128514;``` |
| &#128515; | ```&#128515;``` |
| &#128516; | ```&#128516;``` |
| &#128517; | ```&#128517;``` |
