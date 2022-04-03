---
layout: post
title: HTML 38. 인풋 타입 (Input Types)
subtitle: 이 장에서는 HTML input 요소의 다양한 유형에 대해 설명합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 인풋 타입

## HTML 인풋 타입

다음은 HTML에서 사용할 수 있는 다양한 입력 유형입니다.

+ ```<input type="button">```
+ ```<input type="checkbox">```
+ ```<input type="color">```
+ ```<input type="date">```
+ ```<input type="datetime-local">```
+ ```<input type="email">```
+ ```<input type="file">```
+ ```<input type="hidden">```
+ ```<input type="image">```
+ ```<input type="month">```
+ ```<input type="number">```
+ ```<input type="password">```
+ ```<input type="radio">```
+ ```<input type="range">```
+ ```<input type="reset">```
+ ```<input type="search">```
+ ```<input type="submit">```
+ ```<input type="tel">```
+ ```<input type="text">```
+ ```<input type="time">```
+ ```<input type="url">```
+ ```<input type="week">```

{: .box-note}
**Tip:** ```type``` 속성의 기본값은 "text"입니다.

## input type text

```<input type="text">```는 **한 줄의 텍스트 입력 필드**를 정의합니다.

###### 예제 1

```html
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname">
</form>
```

위의 HTML 코드가 브라우저에 표시되는 방법은 다음과 같습니다

<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname">
</form>

## input type password

```<input type="password">```는 **비밀번호 필드**를 정의합니다.

###### 예제 2

```html
<form>
  <label for="username">Username:</label><br>
  <input type="text" id="username" name="username"><br>
  <label for="pwd">Password:</label><br>
  <input type="password" id="pwd" name="pwd">
</form>
```

위의 HTML 코드가 브라우저에 표시되는 방법은 다음과 같습니다.

<form>
  <label for="username">Username:</label><br>
  <input type="text" id="username" name="username"><br>
  <label for="pwd">Password:</label><br>
  <input type="password" id="pwd" name="pwd">
</form>

{: .box-note}
암호 필드의 문자는 마스킹됩니다(별표 또는 원으로 표시됨).

## input type submit

```<input type="submit">```은 폼 데이터를 **폼 핸들러**에 **제출**하기 위한 버튼을 정의합니다.

폼 핸들러는 일반적으로 입력 데이터를 처리하는 스크립트가 있는 서버 페이지입니다.

폼 핸들러는 폼의 ```action``` 속성에 지정되어 있습니다.

###### 예제 3

```html
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form>
```

위의 HTML 코드가 브라우저에 표시되는 방법입니다.

<form action="https://www.w3schools.com/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form>

```submit``` 버튼의 값 속성을 생략하면 버튼에 기본 텍스트가 표시됩니다.

###### 예제 4

```html
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit">
</form>
```

## input type reset

```<input type="reset">```은 모든 폼 값을 기본값으로 리셋하는 **리셋버튼**을 정의합니다.

###### 예제 5

```html
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit">
  <input type="reset">
</form>
```

위의 HTML 코드가 브라우저에 표시되는 방법은 다음과 같습니다.

<form action="https://www.w3schools.com/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit">
  <input type="reset">
</form>

{: .box-note}
입력값을 변경한 후 "Reset" 버튼을 클릭하면 폼 데이터가 기본값으로 재설정됩니다.

## input type radio

```<input type="radio">```는 **라디오 버튼**을 정의합니다.

라디오 버튼을 사용하면 제한된 수의 선택 항목 중 하나만 선택할 수 있습니다.

###### 예제 6

```html
<p>Choose your favorite Web language:</p>

<form>
  <input type="radio" id="html" name="fav_language" value="HTML">
  <label for="html">HTML</label><br>
  <input type="radio" id="css" name="fav_language" value="CSS">
  <label for="css">CSS</label><br>
  <input type="radio" id="javascript" name="fav_language" value="JavaScript">
  <label for="javascript">JavaScript</label>
</form>
```

위의 HTML 코드가 브라우저에 표시되는 방법은 다음과 같습니다.

<p>Choose your favorite Web language:</p>

<form>
  <input type="radio" id="html" name="fav_language" value="HTML">
  <label for="html">HTML</label><br>
  <input type="radio" id="css" name="fav_language" value="CSS">
  <label for="css">CSS</label><br>
  <input type="radio" id="javascript" name="fav_language" value="JavaScript">
  <label for="javascript">JavaScript</label>
</form>

## input type checkbox

```<input type="checkbox">```는 **체크박스**를 정의합니다.

이 확인란을 사용하면 사용자가 제한된 수의 선택 항목 중 0개 또는 여러 개의 옵션을 선택할 수 있습니다.

###### 예제 7

```html
<form>
  <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
  <label for="vehicle1"> I have a bike</label><br>
  <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
  <label for="vehicle2"> I have a car</label><br>
  <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
  <label for="vehicle3"> I have a boat</label>
</form>
```

위의 HTML 코드가 브라우저에 표시되는 방법은 다음과 같습니다.

<form>
  <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
  <label for="vehicle1"> I have a bike</label><br>
  <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
  <label for="vehicle2"> I have a car</label><br>
  <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
  <label for="vehicle3"> I have a boat</label>
</form>

## input type button

```<input type="button">```은 **버튼**을 정의합니다.

###### 예제 8

```html
<input type="button" onclick="alert('Hello World!')" value="Click Me!">
```

위의 HTML 코드가 브라우저에 표시되는 방법은 다음과 같습니다.

<input type="button" onclick="alert('Hello World!')" value="Click Me!">

## input type color

```<input type="color">```는 색상을 포함해야 하는 입력 필드에 사용됩니다.

브라우저 지원에 따라 색상 선택기가 입력 필드에 표시될 수 있습니다.

###### 예제 9

```html
<form>
  <label for="favcolor">Select your favorite color:</label>
  <input type="color" id="favcolor" name="favcolor">
</form>
```

## input type date

```<input type="date">```는 날짜를 포함해야 하는 입력 필드에 사용됩니다.

브라우저 지원에 따라 달력 선택기가 입력 필드에 표시될 수 있습니다.

###### 예제 10

```html
<form>
  <label for="birthday">Birthday:</label>
  <input type="date" id="birthday" name="birthday">
</form>
```

```min``` 및 ```max``` 속성을 사용하여 날짜에 제한을 추가할 수도 있습니다.

###### 예제 11

```html
<form>
  <label for="datemax">Enter a date before 1980-01-01:</label>
  <input type="date" id="datemax" name="datemax" max="1979-12-31"><br><br>
  <label for="datemin">Enter a date after 2000-01-01:</label>
  <input type="date" id="datemin" name="datemin" min="2000-01-02">
</form>
```

## input type datetime-local

```<input type="datetime-local">```은 날짜 및 시간 입력 필드를 지정합니다. 시간대는 지정하지 않습니다.

브라우저 지원에 따라 달력 선택기가 입력 필드에 표시될 수 있습니다.

###### 예제 12

```html
<form>
  <label for="birthdaytime">Birthday (date and time):</label>
  <input type="datetime-local" id="birthdaytime" name="birthdaytime">
</form>
```

## input type email

```<input type="email">```은 전자 메일 주소를 포함할 필요가 있는 입력 필드에 사용됩니다.

브라우저 지원에 따라서는, 송신시에 전자 메일 주소를 자동적으로 검증할 수 있습니다.

일부 스마트폰은 이메일 유형을 인식하고 이메일 입력과 일치하도록 키보드에 ".com"을 추가합니다.

###### 예제 13

```html
<form>
  <label for="myfile">Select a file:</label>
  <input type="file" id="myfile" name="myfile">
</form>
```

## input type hidden

```<input type="hidden">```은 숨겨진 입력 필드(사용자에게는 표시되지 않음)를 정의합니다.

숨김 필드를 통해 웹 개발자는 양식을 제출할 때 사용자가 보거나 수정할 수 없는 데이터를 포함할 수 있습니다.

숨김 필드는 양식을 제출할 때 업데이트해야 하는 데이터베이스 레코드를 저장하는 경우가 많습니다.

{: .box-note}
이 값은 페이지 내용에서 사용자에게 표시되지 않지만 브라우저의 개발자 도구 또는 "소스 보기" 기능을 사용하여 볼 수 있으며 편집할 수 있습니다. 숨겨진 입력을 보안의 형태로 사용하지 마십시오.

###### 예제 14

```html
<form>
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <input type="hidden" id="custId" name="custId" value="3487">
  <input type="submit" value="Submit">
</form>
```

## input type month

```<input type="month">```에서는 월과 연도를 선택할 수 있습니다.

브라우저 지원에 따라 달력 선택기가 입력 필드에 표시될 수 있습니다.

###### 예제 15

```html
<form>
  <label for="bdaymonth">Birthday (month and year):</label>
  <input type="month" id="bdaymonth" name="bdaymonth">
</form>
```

## input type number

```<input type="number">```는 숫자 입력 필드를 정의합니다.

허가되는 번호에 제한을 설정할 수도 있습니다.

다음 예제에서는 1 ~5 의 값을 입력할 수 있는 숫자 입력 필드를 표시합니다.

###### 예제 16

```html
<form>
  <label for="quantity">Quantity (between 1 and 5):</label>
  <input type="number" id="quantity" name="quantity" min="1" max="5">
</form>
```

## input 제한

다음은 일반적인 입력 제한 사항 목록입니다.

| 속성 | 설명 |
| checked | 페이지가 로드될 때 입력 필드를 미리 선택하도록 지정합니다(type="checkbox" 또는 type="radio"의 경우). |
| disabled | 입력 필드를 비활성화하도록 지정합니다. |
| max | 입력 필드의 최대값을 지정합니다. |
| maxlength | 입력 필드의 최대 문자 수를 지정합니다. |
| min | 입력 필드의 최소값을 지정합니다. |
| pattern | 입력 값을 확인할 정규 표현을 지정합니다. |
| readonly | 입력 필드를 읽기 전용으로 지정합니다(변경할 수 없음). |
| required | 입력 필드를 입력해야 함을 지정합니다(필수 입력). |
| size | 입력 필드의 너비(문자 단위)를 지정합니다. |
| step | 입력 필드의 올바른 번호 간격을 지정합니다. |
| value | 입력 필드의 기본값을 지정합니다. |

다음은 숫자 입력 필드를 표시하는 예를 나타냅니다. 이 필드에서는 0 ~100 의 값을 10 의 순서로 입력할 수 있습니다. 기본값은 30 입니다.

###### 예제 17

```html
<form>
  <label for="quantity">Quantity:</label>
  <input type="number" id="quantity" name="quantity" min="0" max="100" step="10" value="30">
</form>
```

## input type range

```<input type="range">```는 정확한 값이 중요하지 않은 숫자(슬라이더 컨트롤 등)를 입력하기 위한 컨트롤을 정의합니다. 기본 범위는 0 ~100 입니다. 단, ```min```, ```max``` 및 ```step``` 속성을 사용하여 허용되는 숫자에 대한 제한을 설정할 수 있습니다.

###### 예제 18

```html
<form>
  <label for="vol">Volume (between 0 and 50):</label>
  <input type="range" id="vol" name="vol" min="0" max="50">
</form>
```

## input type search

```<input type="search">```는 검색 필드에 사용됩니다(검색 필드는 일반 텍스트 필드처럼 작동합니다).

###### 예제 20

```html
<form>
  <label for="gsearch">Search Google:</label>
  <input type="search" id="gsearch" name="gsearch">
</form>
```

## input type tel

```<input type="tel">```은 전화번호를 포함해야 하는 입력 필드에 사용됩니다.

###### 예제 21

```html
<form>
  <label for="phone">Enter your phone number:</label>
  <input type="tel" id="phone" name="phone" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}">
</form>
```

## input type time

```<input type="time">```을 사용하면 사용자가 시간(타임존 없음)을 선택할 수 있습니다.

브라우저 지원에 따라 시간 선택기가 입력 필드에 표시될 수 있습니다.

###### 예제 22

```html
<form>
  <label for="appt">Select a time:</label>
  <input type="time" id="appt" name="appt">
</form>
```

## input type url

```<input type="url">```은 URL 주소를 포함해야 하는 입력 필드에 사용됩니다.

브라우저 지원에 따라 url 필드는 전송 시 자동으로 검증될 수 있습니다.

일부 스마트폰은 URL 유형을 인식하여 키보드에 .com을 추가하여 URL 입력과 일치시킵니다.

###### 예제 23

```html
<form>
  <label for="homepage">Add your homepage:</label>
  <input type="url" id="homepage" name="homepage">
</form>
```

## input type week

```<input type="week">``` 를 사용하면 사용자는 요일과 연도를 선택할 수 있습니다.

브라우저 지원에 따라 달력 선택기가 입력 필드에 표시될 수 있습니다.

###### 예제 24

```html
<form>
  <label for="week">Select a week:</label>
  <input type="week" id="week" name="week">
</form>
```
