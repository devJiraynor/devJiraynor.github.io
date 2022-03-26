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

###### 예제 5

```html
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" size="50"><br>
  <label for="pin">PIN:</label><br>
  <input type="text" id="pin" name="pin" maxlength="4" size="4">
</form>
```

## ```min```과 ```max``` 속성

input ```min``` 및 ```max``` 속성은 입력 필드의 최소 및 최대 값을 지정합니다.

```min``` 및 ```max``` 속성은 number, range, date, datetime-local, month, time 및 week 입력 type으로 작동합니다.

{: .box-note}
```max``` 속성과 ```min``` 속성을 함께 사용하여 가능한 값의 범위를 만듭니다.

###### 예제 6

```html
<form>
  <label for="datemax">Enter a date before 1980-01-01:</label>
  <input type="date" id="datemax" name="datemax" max="1979-12-31"><br><br>

  <label for="datemin">Enter a date after 2000-01-01:</label>
  <input type="date" id="datemin" name="datemin" min="2000-01-02"><br><br>

  <label for="quantity">Quantity (between 1 and 5):</label>
  <input type="number" id="quantity" name="quantity" min="1" max="5">
</form>
```

## ```multiple``` 속성

input ```multiple``` 속성은 사용자가 입력 필드에 여러 값을 입력할 수 있도록 지정합니다.

```multiple``` 속성은 이메일 및 파일 입력 유형과 함께 작동합니다.

###### 예제 6

```html
<form>
  <label for="files">Select files:</label>
  <input type="file" id="files" name="files" multiple>
</form>
```

## ```pattern``` 속성

input ```pattern``` 속성은 양식을 제출할 때 입력 필드의 값을 확인할 정규식을 지정합니다.

```pattern``` 속성은 text, date, search, URL, tel, email 및 password 입력 type으로 작동합니다.

###### 예제 7

```html
<form>
  <label for="country_code">Country code:</label>
  <input type="text" id="country_code" name="country_code"
  pattern="[A-Za-z]{3}" title="Three letter country code">
</form>
```

## ```placeholder``` 속성

input ```placeholder``` 속성은 입력 필드의 예상 값을 설명하는 짧은 힌트(예측된 형식의 샘플 값 또는 짧은 설명)를 지정합니다.

사용자가 값을 입력하기 전에 입력 필드에 짧은 힌트가 표시됩니다.

```placeholder``` 속성은 text, search, URL, tel, email 및 password 입력 type으로 작동합니다.

###### 예제 8

```html
<form>
  <label for="phone">Enter a phone number:</label>
  <input type="tel" id="phone" name="phone"
  placeholder="123-45-678"
  pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}">
</form>
```

## ```required``` 속성

input ```required``` 속성은 폼을 전송하기 전에 입력 필드를 입력해야 함을 지정합니다.

```required``` 속성은 text, search, URL, tel, email, password, date picker, number, checkbox, radio 및 file 입력 type으로 작동합니다.

###### 예제 9

```html
<form>
  <label for="username">Username:</label>
  <input type="text" id="username" name="username" required>
</form>
```

## ```step``` 속성

input ```step``` 속성은 입력 필드의 정규 번호 간격을 지정합니다.

예: step="3"인 경우 가능한 수는 -3, 0, 3, 6 등이 될 수 있습니다.

{: .box-note}
이 속성은 ```max``` 및 ```min``` 속성과 함께 사용하여 유효한 값의 범위를 작성할 수 있습니다.

```step``` 속성은 number, range, date, datetime-local, month, date 및 week 입력 type으로 작동합니다.

###### 예제 10

```html
<form>
  <label for="points">Points:</label>
  <input type="number" id="points" name="points" step="3">
</form>
```

{: .box-bote}
**Note:** 입력 제한은 오류 방지 기능이 아니며 JavaScript는 잘못된 입력을 추가할 수 있는 많은 방법을 제공합니다. 입력을 안전하게 제한하려면 수신자(서버)도 확인해야 합니다!

## ```autofocus``` 속성

input ```autofocus``` 속성은 페이지가 로드될 때 입력 필드가 자동으로 포커스를 받도록 지정합니다.

###### 예제 11

```html
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" autofocus><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname">
</form>
```

## ```height```와 ```width``` 속성

input ```height``` 및 ```width``` 속성은 ```<input type="image">``` 요소의 높이 및 폭을 지정합니다.

{: .box-note}
**Tip:** 이미지의 높이와 너비 속성을 항상 지정하십시오. 높이와 폭이 설정된 경우 페이지가 로드될 때 이미지에 필요한 공간이 예약됩니다. 이러한 속성이 없으면 브라우저는 이미지의 크기를 알 수 없으며 적절한 공간을 예약할 수 없습니다. 그 결과 로드 중에(이미지가 로드되는 동안) 페이지 레이아웃이 변경됩니다.

###### 예제 12

```html
<form>
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname"><br><br>
  <input type="image" src="img_submit.gif" alt="Submit" width="48" height="48">
</form>
```

## ```list``` 속성

input ```list``` 속성은 ```<input>``` 요소의 사전 정의된 옵션을 포함하는 ```<datalist>``` 요소를 참조합니다.

###### 예제 13

```html
<form>
  <input list="browsers">
  <datalist id="browsers">
    <option value="Internet Explorer">
    <option value="Firefox">
    <option value="Chrome">
    <option value="Opera">
    <option value="Safari">
  </datalist>
</form>
```

## ```autocomplete``` 속성

input ```autocomplete``` 속성은 폼 또는 입력 필드의 자동 완성을 켜거나 끌지 여부를 지정합니다.

자동 완료를 사용하면 브라우저가 값을 예측할 수 있습니다. 사용자가 필드에 입력하기 시작하면 브라우저는 이전에 입력한 값을 기준으로 필드를 입력하는 옵션을 표시해야 합니다.

```autocomplete``` 속성은 ```<form>``` 및 text, search, URL, tel, email, password, date picker, range 및 color의 ```<input>``` 유형으로 동작합니다.

###### 예제 14

```html
<form action="/action_page.php" autocomplete="on">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname"><br><br>
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" autocomplete="off"><br><br>
  <input type="submit" value="Submit">
</form>
```

{: .box-note}
일부 브라우저에서는 이 기능이 작동하려면 자동 완성 기능을 활성화해야 할 수 있습니다.
