---
layout: post
title: CSS 36. 속성 셀렉터 (Attribute Selectors)
subtitle: 속성 셀렉터는 지정된 속성을 가진 요소를 선택하는 데 사용됩니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 속성 셀렉터

## 특정 특성을 사용하여 HTML 요소 스타일 지정

특정 속성 또는 속성 값을 가진 HTML 요소를 스타일링할 수 있습니다.

## ```[attribute]``` 셀렉터

```[attribute]``` 셀렉터는 지정된 속성을 가진 요소를 선택하는 데 사용됩니다.

다음 예제에서는 대상 특성을 가진 모든 ```<a>``` 요소를 선택합니다.

###### 예제 1

```css
a[target] {
  background-color: yellow;
}
```

## ```[attribute="value"]``` 셀렉터

```[attribute="value"]``` 셀렉터는 지정된 속성 및 값을 가진 요소를 선택하는 데 사용됩니다.

다음 예제에서는 ```target="_blank"``` 특성을 가진 모든 ```<a>``` 요소를 선택합니다.

###### 예제 2

```css
a[target="_blank"] {
  background-color: yellow;
}
```

## ```[attribute~="value"]``` 셀렉터

```[attribute~="value"]``` 셀렉터는 지정된 단어를 포함하는 속성 값을 가진 요소를 선택하는 데 사용됩니다.

다음 예제에서는 공백으로 구분된 단어 목록을 포함하는 제목 속성을 가진 모든 요소를 선택합니다.

###### 예제 3

```css
[title~="flower"] {
  border: 5px solid yellow;
}
```

위의 예제는 title="flower", title="summer flower" 및 title="flower new"의 요소와 일치하지만 title="my-flower" 또는 title="flower"는 일치하지 않습니다.

## ```[attribute|="value"]``` 셀렉터

```[attribute|="value"]``` 셀렉터는 값이 정확히 지정된 값 또는 하이픈(-) 뒤에 오는 지정된 값을 가진 요소를 선택하는 데 사용됩니다.

**Note:** 값은 class="top"과 같이 단어 전체를 단독으로 사용하거나, class="top-text"와 같이 하이픈( -)이 뒤에 와야 합니다.

###### 예제 4

```css
[class|="top"] {
  background: yellow;
}
```

## ```[attribute^="value"]``` 셀렉터

```[attribute^="value"]``` 셀렉터는 지정된 속성으로 값이 지정된 값으로 시작하는 요소를 선택하는 데 사용됩니다.

다음 예제에서는 "top"으로 시작하는 클래스 속성 값을 가진 모든 요소를 선택합니다.

**Note:** 값은 완벽한 단어일 필요는 없습니다!

###### 예제 5

```css
[class^="top"] {
  background: yellow;
}
```

## ```[attribute$="value"]``` 셀렉터

```[attribute$="value"]``` 셀렉터는 속성 값이 지정된 값으로 끝나는 요소를 선택하는 데 사용됩니다.

다음 예제에서는 "test"로 끝나는 클래스 속성 값을 가진 모든 요소를 선택합니다.

**Note:** 값은 완벽한 단어일 필요는 없습니다!

###### 예제 6

```css
[class$="test"] {
  background: yellow;
}
```

## ```[attribute*="value"]``` 셀렉터

```[attribute*="value"]``` 셀렉터는 속성 값이 지정된 값을 포함하는 요소를 선택하는 데 사용됩니다.

다음 예제에서는 "te"를 포함하는 클래스 속성 값을 가진 모든 요소를 선택합니다.

**Note:** 값은 완벽한 단어일 필요는 없습니다!

###### 예제 7

```css
[class*="te"] {
  background: yellow;
}
```

## 스타일링 양식

속성 셀렉터는 클래스나 ID가 없는 폼을 스타일링하는 데 유용할 수 있습니다.

###### 예제 8

```css
input[type="text"] {
  width: 150px;
  display: block;
  margin-bottom: 10px;
  background-color: yellow;
}

input[type="button"] {
  width: 120px;
  margin-left: 35px;
  display: block;
}
```
