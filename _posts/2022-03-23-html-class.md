---
layout: post
title: HTML 18. 클래스 (class)
subtitle: HTML class 속성은 HTML 요소의 클래스를 지정하는 데 사용됩니다. 여러 HTML 요소가 동일한 클래스를 공유할 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML class 속성

## class 속성 사용

```class``` 속성은 스타일 시트에서 클래스 이름을 가리키는 데 자주 사용됩니다. 또한 JavaScript에서 특정 클래스 이름을 가진 요소에 액세스하여 조작할 수도 있습니다.

다음 예제에서는 "city" 값을 가진 ```class``` 속성을 가진 3개의 ```<div>``` 요소가 있습니다. 3개의 ```<div>``` 요소는 모두 헤드 섹션의 ```.city``` 스타일 정의에 따라 동일하게 스타일링됩니다.

###### 예제 1

```html
<!DOCTYPE html>
<html>
<head>
<style>
.city {
  background-color: tomato;
  color: white;
  border: 2px solid black;
  margin: 20px;
  padding: 20px;
}
</style>
</head>
<body>

<div class="city">
  <h2>London</h2>
  <p>London is the capital of England.</p>
</div>

<div class="city">
  <h2>Paris</h2>
  <p>Paris is the capital of France.</p>
</div>

<div class="city">
  <h2>Tokyo</h2>
  <p>Tokyo is the capital of Japan.</p>
</div>

</body>
</html>
```

다음 예제에서는 "note" 값을 가진 ```class``` 속성을 가진 2개의 ```<span>``` 요소가 있습니다. 두 ```<span>``` 요소는 헤드 섹션의 ```.note``` 스타일 정의에 따라 동일하게 스타일링됩니다.

###### 예제 2

```html
<!DOCTYPE html>
<html>
<head>
<style>
.note {
  font-size: 120%;
  color: red;
}
</style>
</head>
<body>

<h1>My <span class="note">Important</span> Heading</h1>
<p>This is some <span class="note">important</span> text.</p>

</body>
</html>
```

{: .box-note}
**Tip:** ```class``` 속성은 모든 HTML 요소에서 사용할 수 있습니다.

{: .box-note}
**Note:** 클래스 이름은 대소문자를 구분합니다!

## class 구문

클래스를 만들려면 마침표(.) 문자 뒤에 클래스 이름을 입력합니다. 그런 다음 중괄호 {} 내에서 CSS 속성을 정의하십시오.

###### 예제 3 - city 이름의 class 만들기

```html
<!DOCTYPE html>
<html>
<head>
<style>
.city {
  background-color: tomato;
  color: white;
  padding: 10px;
}
</style>
</head>
<body>

<h2 class="city">London</h2>
<p>London is the capital of England.</p>

<h2 class="city">Paris</h2>
<p>Paris is the capital of France.</p>

<h2 class="city">Tokyo</h2>
<p>Tokyo is the capital of Japan.</p>

</body>
</html>
```

## 복수 클래스

HTML 요소는 여러 클래스에 속할 수 있습니다.

여러 클래스를 정의하려면 클래스 이름을 공백으로 구분합니다(예: <div class="city main">). 요소는 지정된 모든 클래스에 따라 스타일링됩니다.

다음 예제에서는 첫 번째 ```<h2>``` 요소는 ```city``` 클래스와 ```main``` 클래스 모두에 속하며 두 클래스 모두에서 CSS 스타일을 가져옵니다.

###### 예제 4
  
```html
<h2 class="city main">London</h2>
<h2 class="city">Paris</h2>
<h2 class="city">Tokyo</h2>
```
  
## 여러 요소가 동일한 클래스를 공유할 수 있음
  
다른 HTML 요소가 동일한 클래스 이름을 가리킬 수 있습니다.

다음 예에서는 ```<h2```>와 ```<p>``` 모두 "city" 클래스를 가리키며 동일한 스타일을 공유합니다.
  
###### 예제 5
  
```html
<h2 class="city">Paris</h2>
<p class="city">Paris is the capital of France</p>
```

## JavaScript에서의 클래스 속성 사용
  
클래스 이름은 JavaScript에서 특정 요소에 대한 특정 작업을 수행하기 위해 사용할 수도 있습니다.

JavaScript는 ```getElementsByClassName()``` 메서드를 사용하여 특정 클래스 이름을 가진 요소에 액세스할 수 있습니다.
  
###### 예제 6 - 클래스 이름이 "city"인 모든 요소를 숨기려면 버튼을 클릭
  
```html
<script>
function myFunction() {
  var x = document.getElementsByClassName("city");
  for (var i = 0; i < x.length; i++) {
    x[i].style.display = "none";
  }
}
</script>
 
```

## Summary

+ HTML ```class``` 속성은 요소의 하나 이상의 클래스 이름을 지정합니다.
+ 클래스는 CSS 및 JavaScript에서 특정 요소를 선택하고 액세스하기 위해 사용됩니다.
+ ```class``` 속성은 모든 HTML 요소에서 사용할 수 있습니다.
+ 클래스 이름은 대소문자를 구분합니다.
+ 다른 HTML 요소가 동일한 클래스 이름을 가리킬 수 있습니다.
+ JavaScript는 ```getElementsByClassName()``` 메서드를 사용하여 특정 클래스 이름을 가진 요소에 액세스할 수 있습니다.

