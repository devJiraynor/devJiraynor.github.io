---
layout: post
title: CSS 30. 유사 요소 (Pseudo-elements)
subtitle: CSS 유사 요소에 대해 알아봅니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 유사 요소 (Pseudo-elements)

## 유사 요소란?

CSS 유사 요소는 요소의 지정된 부분을 스타일링하는 데 사용됩니다.

예를 들어 다음과 같은 용도로 사용할 수 있다.

+ 요소의 첫 번째 문자 또는 라인 스타일 지정
+ 요소의 내용 앞이나 뒤에 내용 삽입

## 구문

유사 요소의 구문:

```css
selector::pseudo-element {
  property: value;
}
```

## ```::first-line``` 유사 요소

```::first-line``` 유사 요소는 텍스트의 첫 번째 줄에 특수 스타일을 추가하는 데 사용됩니다.

다음은 모든 ```<p>``` 요소에서 텍스트의 첫 번째 줄을 포맷하는 예제입니다.

###### 예제 1

```css
p::first-line {
  color: #ff0000;
  font-variant: small-caps;
}
```

**Note:** ```::first-line``` 유사 요소는 블록 수준 요소에만 적용할 수 있습니다.

다음 속성은 ```::first-line``` 유사 요소에 적용됩니다.

+ ```font``` 속성
+ ```color``` 속성 
+ ```background``` 속성
+ ```margin``` 속성
+ ```padding``` 속성
+ ```border``` 속성
+ ```text-decoration```
+ ```vertical-align```("float"이 "none"인 경우에만 해당)
+ ```text-transform```
+ ```line-height```
+ ```float```
+ ```clear```

## 유사 요소와 HTML 클래스

유사 요소는 HTML 클래스와 결합할 수 있습니다.

###### 예제 2

```css
p.intro::first-letter {
  color: #ff0000;
  font-size: 200%;
}
```

위의 예제는 class="intro"를 가진 문단의 첫 글자를 빨간색과 더 큰 크기로 표시합니다.

## 다중 유사 요소

여러 유사 요소를 결합할 수도 있습니다.

다음 예제에서 문단의 첫 글자는 xx-large 글꼴 크기로 빨간색입니다. 첫 번째 줄의 나머지 부분은 파란색이며 small-cap으로 표시됩니다. 문단의 나머지 부분은 기본 글꼴 크기 및 색상이 됩니다.

###### 예제 3

```css
p::first-letter {
  color: #ff0000;
  font-size: xx-large;
}

p::first-line {
  color: #0000ff;
  font-variant: small-caps;
}
```
