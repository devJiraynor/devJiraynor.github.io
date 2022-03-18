---
layout: post
title: HTML 5.단락(Paragrap)
subtitle: HTML 단락은 항상 새 행에서 시작하며 일반적으로 텍스트 블록입니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---
   
# HTML 단락   
   
## HTML 단락   
   
HTML ```<p>``` 요소는 문단을 정의합니다.

단락은 항상 새 줄에서 시작되며, 브라우저는 단락의 앞뒤에 공백(여백)을 자동으로 추가합니다.

###### 예제 1

```html
<p>첫번째 단락입니다.</p>
<p>두번째 단락입니다.</p>
```

## HTML 표시

HTML이 어떻게 표시되는지 알 수 없습니다.

화면이 크거나 작거나 크기가 조정된 창은 다른 결과를 생성합니다.

HTML에서는 HTML 코드에 공백이나 행을 추가하여 표시를 변경할 수 없습니다.

브라우저는 페이지가 표시될 때 추가 공간과 행을 자동으로 제거합니다.

###### 예제 2

```html
<p>
이 단락은 소스코드에 
많은 행이 포함되어 있습니다.
브라우저는 
무시합니다.
</p>

<p>
이  단락은 소스코드에 
많은 행이 포함되어  있습니다.
브라우저는 
무시합니다.
</p>
```

## HTML Horizontal Rules

```<hr>``` 태그는 HTML 페이지의 주제 구분을 정의하며, 대부분의 경우 수평 규칙으로 표시됩니다.

```<hr>``` 요소는 HTML 페이지에서 콘텐츠를 구분(또는 변경 정의)하기 위해 사용됩니다.

###### 예제 3

```html
<h1>This is heading 1</h1>
<p>This is some text.</p>
<hr>
<h2>This is heading 2</h2>
<p>This is some other text.</p>
<hr>
```

```<hr>``` 태그는 빈 태그입니다.즉, 종료 태그가 없습니다.
