---
layout: post
title: CSS 03. 셀렉터 (Selector)
subtitle: CSS 실렉터는 스타일링할 HTML 요소를 선택합니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 셀렉터

## CSS 셀렉터

CSS 실렉터는 스타일링할 HTML 요소를 "선택"하기 위해 사용됩니다.

CSS 실렉터는 5개의 카테고리로 나눌 수 있습니다.

+ 단순 셀렉터(이름, ID, 클래스에 따라 요소를 선택)
+ 콤비네이터 셀렉터(특정 관계에 따라 요소를 선택)
+ 유사 클래스 셀렉터(특정 상태에 따라 요소를 선택)
+ 유사 요소 셀렉터(요소의 일부를 선택하고 스타일 지정)
+ 속성 셀렉터(속성 또는 속성 값에 따라 요소를 선택)

이 페이지에서는 가장 기본적인 CSS 셀렉터에 대해 설명합니다.

## CSS 요소 셀렉터

요소 셀렉터는 요소 이름을 기반으로 HTML 요소를 선택합니다.

###### 예제 1 - 여기에서는 페이지의 모든 ```<p>``` 요소가 빨간색 텍스트 색상으로 가운데 정렬됩니다.

```css
p {
  text-align: center;
  color: red;
}
```

## CSS ID 실렉터

+ id 셀렉터는 HTML 요소의 id 속성을 사용하여 특정 요소를 선택합니다.
+ 요소의 ID는 페이지 내에서 고유하므로 id 셀렉터를 사용하여 하나의 고유 요소를 선택합니다.
+ 특정 id를 가지는 요소를 선택하려면, 해시(#) 문자 뒤에 요소의 id를 입력합니다.

###### 예제 2 - 아래 CSS 규칙은 ```id="display1"```인 HTML 요소에 적용됩니다.

```css
#para1 {
  text-align: center;
  color: red;
}
```

{: .box-note}
**Note:** id 이름은 숫자로 시작할 수 없습니다!

## CSS class 셀렉터

class 셀렉터는 특정 클래스 속성을 가진 HTML 요소를 선택합니다.

특정 클래스의 요소를 선택하려면 마침표(.) 문자 뒤에 클래스 이름을 입력합니다.

###### 예제 3 - 이 예에서는 ```class="center"```인 모든 HTML 요소가 빨간색으로 가운데 정렬됩니다.

```css
.center {
  text-align: center;
  color: red;
}
```

특정 HTML 요소만 클래스의 영향을 받도록 지정할 수도 있습니다.

###### 예제 4 - 이 예에서는 ```class="center"```인 ```<p>``` 요소만 빨간색으로 가운데 정렬됩니다.

```css
p.center {
  text-align: center;
  color: red;
}
```

HTML 요소는 여러 클래스를 참조할 수도 있습니다.

###### 예제 5 - 이 예에서 ```<p>``` 요소는 ```class="center"``` 및 ```class="large"```에 따라 스타일링됩니다.

```html
<p class="center large">This paragraph refers to two classes.</p>
```

{: .box-note}
**Note:** 클래스 이름은 숫자로 시작할 수 없습니다!

## CSS 유니버설 셀렉터

유니버설 셀렉터(```*```)는 페이지의 모든 HTML 요소를 선택합니다.

###### 예제 6 - 다음 CSS 규칙은 페이지의 모든 HTML 요소에 영향을 줍니다.

```css
* {
  text-align: center;
  color: blue;
}
```

## CSS 그룹 셀렉터

그룹 선택기는 스타일 정의가 동일한 모든 HTML 요소를 선택합니다.

다음 CSS 코드를 확인합니다(```h1```, ```h2```, 및 ```p``` 요소의 스타일 정의는 동일합니다).

```css
h1 {
  text-align: center;
  color: red;
}

h2 {
  text-align: center;
  color: red;
}

p {
  text-align: center;
  color: red;
}
```

코드를 최소화하기 위해 셀렉터를 그룹화하는 것이 좋습니다.

셀렉터를 그룹화하려면 각 셀렉터를 comma (```,```)로 구분합니다.

###### 예제 7 - 이 예에서는 위의 코드에서 실렉터를 그룹화하고 있습니다.

```css
h1, h2, p {
  text-align: center;
  color: red;
}
```
