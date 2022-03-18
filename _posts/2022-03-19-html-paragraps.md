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
이 단락은      소스코드에 
많은 행이      포함되어 있습니다.
브라우저는 
무시합니다.
</p>
```
