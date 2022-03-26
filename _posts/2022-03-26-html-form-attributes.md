---
layout: post
title: HTML 36. 폼 속성 (Form Attributes)
subtitle:이 장에서는 HTML form 요소의 다양한 속성에 대해 설명합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 폼 속성

## ```action``` 속성

```action``` 속성은 양식을 제출할 때 수행할 작업을 정의합니다.

보통 폼 데이터는 사용자가 Submit 버튼을 클릭하면 서버상의 파일로 송신됩니다.

다음 예제에서는 폼 데이터가 "action_page.php"라는 파일로 전송됩니다. 이 파일에는 폼 데이터를 처리하는 서버측 스크립트가 포함되어 있습니다.

###### 예제 1

```html
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form>
```

{: .box-note}
```action``` 속성을 생략하면 액션은 현재 페이지로 설정됩니다.

## ```target``` 속성

```target``` 속성은 양식을 제출한 후 수신된 응답을 표시할 위치를 지정합니다.

```target``` 속성에는, 다음의 몇개의 값을 지정할 수 있습니다.

| 값 | 설명 |
| ```_blank``` | 응답이 새 창 또는 탭에 표시됩니다. |
| ```_self``` | 응답이 현재 창에 표시됩니다. |
| ```_parent``` | 응답이 부모 프레임에 표시됩니다. |
| ```_top``` | 응답이 창의 전체 본문에 표시됩니다. |
| ```framename``` | 응답이 이름 있는 iframe에 표시됩니다. |

기본값은 ```_self``` 입니다. 이것은 응답이 현재 창에서 열리는 것을 의미합니다.

###### 예제 2

```html
<form action="/action_page.php" target="_blank">
```

## ```method``` 속성

```method``` 속성은 폼 데이터를 제출할 때 사용하는 HTTP 메서드를 지정합니다.

폼 데이터는 URL 변수 (```method="get"```) 또는 HTTP 포스트 트랜잭션(```method="post"```)으로 전송할 수 있습니다.

폼 데이터를 송신할 때의 디폴트의 HTTP 방식은, GET 입니다.

###### 예제 3 - GET 방식 전송

```html
<form action="/action_page.php" method="get">
```

###### 예제 3 - POST 방식 전송

```html
<form action="/action_page.php" method="post">
```

GET 관련 주의사항: 

+ 이름/값 쌍의 URL에 양식 데이터를 추가합니다.
+ GET을 사용하여 기밀 데이터를 전송하지 마십시오! (제출된 폼 데이터는 URL에 표시됩니다!)
+ URL의 길이는 제한되어 있습니다(2048 문자).
+ 사용자가 결과를 북마크하려는 양식 제출에 유용합니다.
+ GET은 Google의 쿼리 문자열과 같이 안전하지 않은 데이터에 적합합니다.

POST 관련 주의사항:

+ HTTP 요청 본문 내에 폼 데이터를 추가합니다(제출된 폼 데이터는 URL에 표시되지 않음).
+ POST에는 사이즈 제한이 없기 때문에, 대량의 데이터를 송신할 수 있습니다.
+ POST가 포함된 양식 제출은 북마크할 수 없습니다.

{: .box-note}
폼 데이터에 기밀 정보나 개인정보가 포함되어 있는 경우는, 항상 POST 를 사용해 주세요.

## ```autocomplete``` 속성

```autocomplete``` 속성은 폼의 자동 완성 여부를 지정합니다.

자동 완성이 켜져 있으면 브라우저는 사용자가 이전에 입력한 값에 따라 자동으로 값을 완성합니다.

###### 예제 4

```html
<form action="/action_page.php" autocomplete="on">
```

## ```novalidate``` 속성

```novalidate``` 속성은 논리 속성입니다

존재하는 경우는 송신시에 폼 데이터(입력)를 검증하지 않는 것을 지정합니다.

###### 예제 5

```html
<form action="/action_page.php" novalidate>
```
