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

## ```form``` 속성

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

## ```formaction``` 속성

input ```formaction``` 속성은 ```form``` 을 제출할 때 입력을 처리할 파일의 URL을 지정합니다.

{: .box-note}
**Note:** 이 속성은 ```<form>``` 요소의 ```action``` 속성을 덮어씁니다.

```formaction``` 속성은 ```submit``` 및 ```image``` input type으로 작동합니다.

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

## ```formenctype``` 속성

input ```formenctpe``` 속성은 제출 시 폼 데이터를 인코딩하는 방법을 지정합니다(```method="post"```인 폼의 경우에만 해당).

{: .box-note}
**Note:** 이 속성은 ```<form>``` 요소의 ```enctype``` 속성을 재정의합니다.

```formenctpe``` 속성은 ```submit``` 및 ```image``` input type으로 작동합니다.

###### 예제 3 - 2개의 송신 버튼이 있는 폼. 첫 번째는 기본 인코딩으로 폼 데이터를 전송하고 두 번째는 "multipart/form-data"로 인코딩된 폼 데이터를 전송합니다.

```html
<form action="/action_page_binary.asp" method="post">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <input type="submit" value="Submit">
  <input type="submit" formenctype="multipart/form-data"
  value="Submit as Multipart/form-data">
</form>
```

## ```formmethod``` 속성

input ```formmethod``` 속성은 액션 URL에 폼 데이터를 송신하기 위한 HTTP 방식을 정의합니다.

{: .box-note}
**Note:** 이 속성은 ```<form>``` 요소의 ```method``` 속성을 덮어씁니다.

```formmethod``` 속성은 ```submit``` 및 ```image``` input type으로 작동합니다.

```form-data```는 URL 변수(http="get") 또는 HTTP 포스트 트랜잭션(http="post")으로 전송할 수 있습니다.

**"get" 메서드에 대한 주의사항:**

+ 이 메서드는 이름/값 쌍의 URL에 양식 데이터를 추가합니다.
+ 이 방법은 사용자가 결과를 북마크하려는 양식 제출에 유용합니다.
+ URL(브라우저에 따라 다름)에 저장할 수 있는 데이터 양에는 제한이 있으므로 모든 폼 데이터가 올바르게 전송될지 확신할 수 없습니다.
+ 중요한 정보를 전달하기 위해 "get" 방법을 사용하지 마십시오. (비밀번호 또는 기타 중요한 정보는 브라우저의 주소 표시줄에 표시됩니다.)

**"post" 메서드에 대한 주의사항:**

+ 이 메서드는 폼 데이터를 HTTP 포스트 트랜잭션으로 전송합니다.
+ "post" 메서드를 사용한 양식 제출은 북마크할 수 없습니다.
+ "post" 메서드는 "get" 메서드보다 견고하고 안전하며 "post"에는 크기 제한이 없습니다.

###### 예제 4 - 2개의 송신 버튼이 있는 폼. 첫 번째는 method="get"으로 폼 데이터를 전송합니다. 두 번째는 method="post"로 폼 데이터를 전송합니다.

```html
<form action="/action_page.php" method="get">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname"><br><br>
  <input type="submit" value="Submit using GET">
  <input type="submit" formmethod="post" value="Submit using POST">
</form>
```

## ```formtarget``` 속성

input ```formtarget``` 속성은 폼 전송 후 수신된 응답을 표시할 위치를 나타내는 이름 또는 키워드를 지정합니다.

{: .box-note}
**Note:** 이 속성은 ```<form>``` 요소의 ```target``` 속성을 덮어씁니다.

```formtarget``` 속성은 ```submit``` 및 ```image``` input type으로 작동합니다.

###### 예제 5 - 2개의 송신 버튼이 있고, 다른 타겟창이 있는 폼

```html
<form action="/action_page.php">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname"><br><br>
  <input type="submit" value="Submit">
  <input type="submit" formtarget="_blank" value="Submit to a new window/tab">
</form>
```

## ```formnovalidate``` 속성

input ```formnovalidate``` 속성은 ```<input>``` 요소가 전송될 때 검증되지 않도록 지정합니다.

{: .box-note}
**Note:** 이 속성은 ```<form>``` 요소의 ```novalidate``` 속성을 덮어씁니다.

```formnovalidate``` 속성은 ```submit``` input type으로 작동합니다.

###### 예제 6 - 2개의 송신 버튼이 있는 폼(검증 유무)

```html
<form action="/action_page.php">
  <label for="email">Enter your email:</label>
  <input type="email" id="email" name="email"><br><br>
  <input type="submit" value="Submit">
  <input type="submit" formnovalidate="formnovalidate"
  value="Submit without validation">
</form>
```

## ```novalidate``` 속성

```novalidate``` 속성은 ```<form>```의 속성입니다

```novalidate```가 있는 경우 전송 시 모든 폼 데이터를 검증하지 않도록 지정합니다.

###### 예제 7 - 송신시에 폼 데이터를 검증하지 않게 지정합니다.

```html
<form action="/action_page.php" novalidate>
  <label for="email">Enter your email:</label>
  <input type="email" id="email" name="email"><br><br>
  <input type="submit" value="Submit">
</form>
```
