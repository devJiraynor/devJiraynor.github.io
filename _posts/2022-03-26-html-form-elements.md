---
layout: post
title: HTML 37. 폼 요소 (Form Elements)
subtitle: 이 장에서는 다양한 HTML 양식 요소에 대해 설명합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<a href="https://youtu.be/0_wx0v52UEs" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 37. 폼 요소 (Form Elements) 영상 보러가기</a>
<br>
<br>

# HTML 폼 요소

## HTML ```<form>``` 요소

HTML ```<form>``` 요소에는 다음 폼 요소를 1개 이상 포함할 수 있습니다.

+ ```<input>```
+ ```<label>```
+ ```<select>```
+ ```<textarea>```
+ ```<button>```
+ ```<fieldset>```
+ ```<legend>```
+ ```<datalist>```
+ ```<output>```
+ ```<option>```
+ ```<optgroup>```

## ```<input>``` 요소

가장 많이 사용되는 폼 요소의 1개는 ```<input>``` 요소입니다.

```<input>``` 요소는 유형 속성에 따라 여러 가지 방법으로 표시할 수 있습니다.

###### 예제 1

```html
<label for="fname">First name:</label>
<input type="text" id="fname" name="fname">
```

## ```<label>``` 요소

```<label>``` 요소는 여러 폼 요소의 라벨을 정의합니다.

```<label>``` 요소는 사용자가 입력 요소에 초점을 맞추면 화면 판독기가 라벨을 크게 읽기 때문에 스크린 판독기 사용자에게 유용합니다.

```<label>``` 요소는 사용자가 ```<label>``` 요소 내의 텍스트를 클릭하면 라디오 버튼/체크박스가 전환되기 때문에 매우 작은 영역(옵션 버튼이나 체크 박스 등)을 클릭하기 어려운 사용자에게도 도움이 됩니다.

```<label>``` 태그의 ```for``` 애트리뷰트는 이들을 바인드하기 위한 ```<input>``` 요소의 ```id``` 애트리뷰트와 같아야 합니다.

## ```<select>``` 요소

```<select>``` 요소는 드롭다운 목록을 정의합니다.

###### 예제 2

```html
<label for="cars">Choose a car:</label>
<select id="cars" name="cars">
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="fiat">Fiat</option>
  <option value="audi">Audi</option>
</select>
```

```<option>``` 요소는 선택 가능한 옵션을 정의합니다.

기본적으로 드롭다운 목록의 첫 번째 항목이 선택되어 있습니다.

미리 선택된 옵션을 정의하려면 ```selected``` 속성을 옵션에 추가합니다.

###### 예제 3

```html
<option value="fiat" selected>Fiat</option>
```

#### 가시 값

```size``` 속성을 사용하여 표시되는 값의 수를 지정합니다.

###### 예제 4

```html
<label for="cars">Choose a car:</label>
<select id="cars" name="cars" size="3">
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="fiat">Fiat</option>
  <option value="audi">Audi</option>
</select>
```

#### 여러 선택 허용

사용자가 여러 값을 선택할 수 있도록 하려면 ```multiple```을 사용합니다.

```html
<label for="cars">Choose a car:</label>
<select id="cars" name="cars" size="4" multiple>
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="fiat">Fiat</option>
  <option value="audi">Audi</option>
</select>
```

## ```<textarea>``` 요소

```<textarea>``` 요소는 여러 줄 입력 필드(텍스트 영역)를 정의합니다.

###### 예제 5

```html
<textarea name="message" rows="10" cols="30">
The cat was playing in the garden.
</textarea>
```

```rows``` 속성은 텍스트 영역에 표시되는 줄 수를 지정합니다.

```cols``` 속성은 텍스트 영역의 가시 폭을 지정합니다.

위의 HTML 코드가 브라우저에 표시되는 방법입니다.

<textarea name="message" rows="10" cols="30">
The cat was playing in the garden.
</textarea>

CSS를 사용하여 텍스트 영역의 크기를 정의할 수도 있습니다.

###### 예제 6

```html
<textarea name="message" style="width:200px; height:600px;">
The cat was playing in the garden.
</textarea>
```

## ```<button>``` 요소

```<button>``` 요소는 클릭 가능한 버튼을 정의합니다.

###### 예제 7

```html
<button type="button" onclick="alert('Hello World!')">Click Me!</button>
```

위의 HTML 코드가 브라우저에 표시되는 방법입니다.

<button type="button" onclick="alert('Hello World!')">Click Me!</button>

{: .box-note}
버튼 요소의 ```type``` 속성을 항상 지정하십시오. 브라우저마다 버튼 요소에 다른 기본 유형을 사용할 수 있습니다.

## ```<fieldset>```와 ```<legend>``` 요소

```<fieldset>``` 요소는 폼에서 관련 데이터를 그룹화하기 위해 사용됩니다.

```<legend>``` 요소는 ```<fieldset>``` 요소의 캡션을 정의합니다.

###### 예제 8

```html
<form action="/action_page.php">
  <fieldset>
    <legend>Personalia:</legend>
    <label for="fname">First name:</label><br>
    <input type="text" id="fname" name="fname" value="John"><br>
    <label for="lname">Last name:</label><br>
    <input type="text" id="lname" name="lname" value="Doe"><br><br>
    <input type="submit" value="Submit">
  </fieldset>
</form>
```

위의 HTML 코드가 브라우저에 표시되는 방법입니다.

<form action="/action_page.php">
  <fieldset>
    <legend>Personalia:</legend>
    <label for="fname">First name:</label><br>
    <input type="text" id="fname" name="fname" value="John"><br>
    <label for="lname">Last name:</label><br>
    <input type="text" id="lname" name="lname" value="Doe"><br><br>
    <input type="submit" value="Submit">
  </fieldset>
</form>

## ```<datalist>``` 요소

```<datalist>``` 요소는 ```<input>``` 요소의 사전 정의된 옵션 목록을 지정합니다.

사용자가 데이터를 입력할 때 미리 정의된 옵션의 드롭다운 목록이 표시됩니다.

```<input>``` 요소의 ```list``` 속성은 ```<datalist>``` 요소의 ```id``` 속성을 참조해야 합니다.

###### 예제 9

```html
<form action="/action_page.php">
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

## ```<output>``` 요소

```<output>``` 요소는 (스크립트에 의해 실행되는 것과 같은) 계산 결과를 나타냅니다.

###### 예제 10

```html
<form action="/action_page.php"
  oninput="x.value=parseInt(a.value)+parseInt(b.value)">
  0
  <input type="range"  id="a" name="a" value="50">
  100 +
  <input type="number" id="b" name="b" value="50">
  =
  <output name="x" for="a b"></output>
  <br><br>
  <input type="submit">
</form>
```
