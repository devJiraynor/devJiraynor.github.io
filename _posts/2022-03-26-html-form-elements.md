---
layout: post
title: HTML 37. 폼 요소 (Form Elements)
subtitle: 이 장에서는 다양한 HTML 양식 요소에 대해 설명합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

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
