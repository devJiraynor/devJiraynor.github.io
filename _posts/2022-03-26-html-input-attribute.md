---
layout: post
title: HTML 39. 인풋 속성 (Input Attribute)
subtitle: 이 장에서는 HTML input 요소의 다양한 속성에 대해 설명합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 인풋 속성

## ```value``` 속성

input ```value``` 속성은 입력 필드의 초기값은 다음과 같습니다.

###### 예제 1

```html
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe">
</form>
```

## ```readonly``` 속성

input ```readonly``` 속성은 입력 필드가 읽기 전용임을 지정합니다.

읽기 전용 입력 필드는 수정할 수 없습니다(단, 사용자는 이 필드를 탭하여 강조 표시하고 해당 입력 필드에서 텍스트를 복사할 수 있습니다).

양식을 제출할 때 읽기 전용 입력 필드 값이 전송됩니다!

###### 예제 2

```html
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John" readonly><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe">
</form>
```

## ```disable``` 속성

input ```disabled``` 속성은 입력 필드를 비활성화로 지정합니다.

비활성화된 입력 필드는 사용할 수 없으며 클릭할 수 없습니다.

비활성화된 입력 필드의 값은 양식을 제출할 때 전송되지 않습니다!

###### 예제 3

```html
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John" disabled><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe">
</form>
```

## ```size``` 속성

input ```size``` 속성은 입력 필드의 표시 너비를 문자 단위로 지정합니다.

size 기본값은 20 입니다.

{: .box-note}
```size``` 속성은 text, search, tel, url, email 및 password 입력 타입으로 작동합니다.

###### 예제 4

```html
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" size="50"><br>
  <label for="pin">PIN:</label><br>
  <input type="text" id="pin" name="pin" size="4">
</form>
```

## ```maxlength``` 속성

input ```maxlength``` 속성은 입력 필드에 허용되는 최대 문자 수를 지정합니다.

{: .box-note}
```maxlength```가 설정되어 있는 경우 입력 필드는 지정된 문자 수보다 많은 문자를 받아들이지 않습니다. 그러나 이 속성은 피드백을 제공하지 않습니다. 따라서 사용자에게 경고하려면 JavaScript 코드를 작성해야 합니다.
