---
layout: post
title: HTML 07. 텍스트 형식 지정 (Text Formatting)
subtitle: HTML에는 특별한 의미를 가진 텍스트를 정의하기 위한 몇 가지 요소가 포함되어 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/69wU3yQ93Oo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<a href="https://youtu.be/FscdpNx1uwA" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 07. 텍스트 형식 지정 (Text Formatting)</a>
<br>
<br>


# HTML 텍스트 형식 지정

## HTML 포맷 요소

서식 요소는 특수 유형의 텍스트를 표시하도록 설계되었습니다.

+ ```<b>``` - 굵은 글씨
+ ```<strong>``` - 중요 텍스트
+ ```<i>``` - 이탤릭체
+ ```<em>``` - 강조 텍스트
+ ```<mark>``` - 마크된 텍스트
+ ```<small>``` - 작은 텍스트
+ ```<del>``` - 삭제된 텍스트
+ ```<ins>``` - 삽입된 텍스트
+ ```<sub>``` - 서브스크립트 텍스트
+ ```<sup>``` - 상위 텍스트

## HTML ```<b>```  와 ```<strong>``` 요소

HTML ```<b>``` 요소에는 굵은 글씨 텍스트가 정의됩니다.

###### 예제 1

```html
<b>이 텍스트는 굵게 표시됩니다.</b>
```

HTML ```<strong>``` 요소는 매우 중요한 텍스트를 정의합니다. 내부의 내용은 일반적으로 굵은 글씨로 표시됩니다.

###### 예제 2

```html
<strong>이 텍스트는 중요합니다!</strong>
```

## HTML ```<i>``` 와 ```<em>``` 요소

HTML ```<i>``` 요소는 대체 음성 또는 무드에서 텍스트의 일부를 정의합니다. 컨텐츠는 일반적으로 이탤릭체로 표시됩니다.

{: .box-note}
**Tip:** ```<i>``` 태그는 기술 용어, 다른 언어로부터의 문구, 생각, 배송지명 등을 나타낼 때 자주 사용됩니다.

###### 예제 3

```html
<i>이 텍스트는 이탤릭체입니다.</i>
```

HTML ```<em>``` 요소는 강조 텍스트를 정의합니다. 내용물은 일반적으로 이탤릭체로 표시됩니다.

{: .box-note}
**Tip:** 스크린 리더는 ```<em>```에 있는 단어들을 언어적 강세로 강조하여 발음할 것입니다.

###### 예제 4

```html
<em>이 텍스트는 강조되어 있습니다.</em>
```

## HTML ```<small>``` 요소

HTML ```<small>``` 요소는 작은 텍스트를 정의합니다.

###### 예제 5

```html
<small>이것은 작은 텍스트입니다.</small>
```

## HTML ```<mark>``` 요소

HTML ```<mark>``` 요소는 마크 또는 강조 표시해야 할 텍스트를 정의합니다.

###### 예제 6

```html
<p>오늘 <mark>우유</mark> 사는 거 잊지 마세요.</p>
```

## HTML ```<del>``` 요소

HTML ```<del>``` 요소는 문서에서 삭제된 텍스트를 정의합니다. 브라우저는 보통 삭제된 텍스트에 줄을 긋습니다.

###### 예제 7

```html
<p>내가 가장 좋아하는 색은 <del>파랑</del>빨강이다.</p>
```

## HTML ```<ins>``` 요소

HTML ```<ins>``` 요소는 문서에 삽입된 텍스트를 정의합니다. 브라우저는 보통 삽입된 텍스트에 밑줄을 긋습니다.

###### 예제 8

```html
<p>내가 가장 좋아하는 색은 <del>파랑</del> <ins>빨강</ins>이다.</p>
```

## HTML ```<sub>``` 요소

HTML ```<sub>``` 요소는 첨자 텍스트를 정의합니다. 첨자 텍스트는 보통 줄의 절반 아래에 표시되며, 더 작은 글꼴로 렌더링될 수 있습니다. 첨자 텍스트는 화학식에 사용할 수 있습니다.

###### 예제 9

```html
<p>H<sub>2</sub>O CO<sub>2</sub></p>
```

## HTML ```<sup>``` 요소

HTML ```<sup>``` 요소는 상위 텍스트를 정의합니다. 윗글자 텍스트는 일반 줄 위에 반자씩 표시되며, 더 작은 글꼴로 렌더링될 수 있습니다. 각주 텍스트는 제곱에 사용할 수 있습니다.

###### 예제 10

```
<p>m<sup>3</sup><p>
```
