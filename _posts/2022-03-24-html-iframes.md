---
layout: post
title: HTML 20. 아이프레임 (Iframe)
subtitle: HTML iframe은 웹 페이지 내의 웹 페이지를 표시하기 위해 사용됩니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<a href="https://youtu.be/-WSILrLz0h4" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 20. 아이프레임 (Iframe) 영상 보러가기</a>
<br>
<br>

# HTML 아이프레임(Iframe)

## HTML 아이프레임 rnans

HTML ```<iframe>``` 태그는 인라인프레임을 지정합니다.

인라인 프레임은 현재 HTML 문서 내에 다른 문서를 포함하기 위해 사용됩니다.

###### 구문

```html
<iframe src="경로" title="설명"></iframe>
```

{: .box-note}
**Tip:** ```<iframe>```에는 항상 ```title``` 속성을 포함하는 것이 좋습니다. 화면 리더가 ```iframe``` 의 내용을 읽을 때 사용합니다.

## Iframe - 높이 및 폭 설정

```height``` 및 ```width``` 속성을 사용하여 ```iframe``` 크기를 지정합니다.

높이와 폭은 기본적으로 픽셀 단위로 지정됩니다.

###### 예제 1

```html
<iframe src="demo_iframe.htm" height="200" width="300" title="Iframe Example"></iframe>
```

또는 ```style``` 속성을 추가하고 CSS ```height``` 및 ```width``` 속성을 사용할 수 있습니다.

###### 예제 2

```html
<iframe src="demo_iframe.htm" style="height:200px;width:300px;" title="Iframe Example"></iframe>
```

## Iframe - 테두리 제거

기본적으로는 iframe 주위에 테두리가 있습니다.

경계를 삭제하려면 ```style``` 속성을 추가하고 CSS ```border``` 속성을 사용합니다.

###### 예제 3

```html
<iframe src="demo_iframe.htm" style="border:none;" title="Iframe Example"></iframe>
```

CSS를 사용하면 iframe 테두리의 크기, 스타일 및 색상을 변경할 수도 있습니다.

###### 예제 4

```html
<iframe src="demo_iframe.htm" style="border:2px solid red;" title="Iframe Example"></iframe>
```

## Iframe - 링크 대상

iframe은 링크의 타깃프레임으로 사용할 수 있습니다.

링크의 ```target``` 속성은 iframe의 ```name``` 속성을 참조해야 합니다.

###### 예제 5

```html
<iframe src="demo_iframe.htm" name="iframe_a" title="Iframe Example"></iframe>

<p><a href="https://www.w3schools.com" target="iframe_a">W3Schools.com</a></p>
```

## Summary

+ HTML ```<iframe>``` 태그는 인라인프레임을 지정합니다.
+ ```src``` 속성은 포함할 페이지의 URL을 정의합니다.
+ 항상 ```title``` 속성 포함(화면 판독기용)
+ ```height``` 및 ```width``` 속성은 iframe의 크기를 지정합니다.
+ iframe 주위의 테두리를 삭제하려면 ```border:none``` 을 사용합니다.
