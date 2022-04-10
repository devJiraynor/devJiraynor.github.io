---
layout: post
title: CSS 38. 카운터 (Counters)
subtitle: CSS 카운터는 CSS 규칙에 의해 값이 증가할 수 있는 CSS에 의해 유지되는 변수입니다. 카운터를 사용하면 문서의 배치에 따라 내용 모양을 조정할 수 있습니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 카운터

## 카운터를 사용한 자동 번호 지정

CSS 카운터는 "변수"와 같습니다. 변수 값은 CSS 규칙(사용 횟수를 추적하는 규칙)에 의해 증가할 수 있습니다.

CSS 카운터를 사용하기 위해 다음 속성을 사용합니다.

+ ```counter-reset``` - 카운터를 만들거나 재설정합니다.
+ ```counter-increment``` - 카운터 값을 증가시킵니다.
+ ```content``` - 생성된 내용을 삽입합니다.
+ ```counter()```, ```counters()``` 함수 - 요소에 카운터 값을 추가합니다.

CSS 카운터를 사용하려면 먼저 ```counter-reset```을 사용하여 생성해야 합니다.

다음 예제에서는 페이지에 대한 카운터를 작성한 다음 각 ```<h2>``` 요소의 카운터 값을 증가시키고 각 ```<h2>``` 요소의 시작 부분에 "Section  <카운터의 값>:"을 추가합니다.

###### 예제 1

```css
body {
  counter-reset: section;
}

h2::before {
  counter-increment: section;
  content: "Section " counter(section) ": ";
}
```

## 카운터 중첩

다음 예제에서는 페이지(섹션)에 대해 하나의 카운터를 만들고 각 ```<h1>``` 요소(하위 섹션)에 대해 하나의 카운터를 만듭니다. "section" 카운터는 "Section <섹션 카운터의 값>"으로 각 ```<h1>``` 요소에 대해 카운트되고 "subsection" 카운터는 "<섹션 카운터의 값>.<하위 섹션 카운터 값>"으로 카운트됩니다.

###### 예제 2

```css
body {
  counter-reset: section;
}

h1 {
  counter-reset: subsection;
}

h1::before {
  counter-increment: section;
  content: "Section " counter(section) ". ";
}

h2::before {
  counter-increment: subsection;
  content: counter(section) "." counter(subsection) " ";
}
```

카운터의 새 인스턴스가 하위 요소에 자동으로 생성되므로 카운터는 윤곽선 리스트를 만드는 데 유용할 수 있습니다. 여기서는 ```counters()``` 함수를 사용하여 여러 중첩 카운터 수준 사이에 문자열을 삽입합니다.

###### 예제 3

```css
ol {
  counter-reset: section;
  list-style-type: none;
}

li::before {
  counter-increment: section;
  content: counters(section,".") " ";
}
```
