---
layout: post
title: CSS 51. 텍스트 효과 (Text Effects)
subtitle: CSS 텍스트 효과 사용법에 대해 알아봅니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 텍스트 효과

## 텍스트 오버플로, 워드랩, 줄 바꿈 규칙, 쓰기 모드

이 장에서는 다음 속성에 대해 알아봅니다.

+ ```text-overflow```
+ ```word-wrap```
+ ```word-break```
+ ```writing-mode```

## Text Overflow

```text-overflow``` 속성은 표시되지 않는 오버플로된 콘텐츠가 사용자에게 시그널링되는 방법을 지정합니다.

###### 예제 1

```css
p.test1 {
  white-space: nowrap;
  width: 200px;
  border: 1px solid #000000;
  overflow: hidden;
  text-overflow: clip;
}

p.test2 {
  white-space: nowrap;
  width: 200px;
  border: 1px solid #000000;
  overflow: hidden;
  text-overflow: ellipsis;
}
```

다음 예제는 요소 위로 마우스를 올렸을 때 오버플로된 내용을 표시하는 방법을 보여 줍니다.

###### 예제 2

```css
div.test:hover {
  overflow: visible;
}
```

## Word Wrapping

```word-wrap``` 속성은 긴 단어를 다음 줄에 줄바꿈할 수 있게 합니다.

###### 예제 3

```css
p {
  word-wrap: break-word;
}
```

## Word Breaking

```word-break``` 속성은 줄 바꿈 규칙을 지정합니다.

###### 예제 4

```css
p.test1 {
  word-break: keep-all;
}

p.test2 {
  word-break: break-all;
}
```

## Writing Mode

```writing-mode``` 속성은 텍스트 행을 수평으로 배치할지 또는 수직으로 배치할지 지정합니다.

###### 예제 5

```css
p.test1 {
  writing-mode: horizontal-tb;
}

span.test2 {
  writing-mode: vertical-rl;
}

p.test2 {
  writing-mode: vertical-rl;
}
```
