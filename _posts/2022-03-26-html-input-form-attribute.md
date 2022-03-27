---
layout: post
title: HTML 40. input 폼 속성 (Input Form Attribute)
subtitle: 이 장에서는 HTML input 요소의 다양한 form 속성에 대해 설명합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML Input 폼 속성

## form 속성

input ```form``` 속성은 ```<input>``` 요소가 속한 형식을 지정합니다.

이 속성의 값은 속성이 속한 ```<form>``` 요소의 ```id``` 속성과 같아야 합니다.

###### 예제 1 - HTML 양식 외부에 위치한 입력 필드(양식의 일부임)

```html
<form action="/action_page.php" id="form1">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <input type="submit" value="Submit">
</form>

<label for="lname">Last name:</label>
<input type="text" id="lname" name="lname" form="form1">
```

## formaction 속성

input ```formaction``` 속성은 ```form``` 을 제출할 때 입력을 처리할 파일의 URL을 지정합니다.

{: .box-note}
이 속성은 ```<form>``` 요소의 ```action``` 속성을 덮어씁니다.

```formaction``` 속성은 ```submit``` 및 ```image``` 입력 유형으로 작동합니다.

###### 예제 2 - HTMl form 내부에 다른 액션을 가진 2개의 제출 버튼이 있습니다.

```html
<form action="/action_page.php">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname"><br><br>
  <input type="submit" value="Submit">
  <input type="submit" formaction="/action_page2.php" value="Submit as Admin">
</form>
```
