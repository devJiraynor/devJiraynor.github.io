---
layout: post
title: HTML 12. 링크 (Links)
subtitle: 링크는 거의 모든 웹 페이지에 있습니다. 링크를 통해 사용자는 페이지 간에 자신의 길을 클릭할 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 링크

## HTML 링크 - 하이퍼링크

HTML 링크는 하이퍼링크입니다.

링크를 누른 후 다른 문서로 이동할 수 있습니다.

마우스를 링크 위로 이동하면 마우스 화살표가 작은 손으로 바뀝니다.

{: .box-note}
**Note:** 링크가 텍스트일 필요는 없습니다. 링크는 이미지 또는 기타 HTML 요소가 될 수 있습니다.

## HTML 링크 - 구문

HTML ```<a>``` 태그는 하이퍼링크를 정의합니다. 구문은 다음과 같습니다.

```html
<a href="url">링크 텍스트</a>
```

```<a>``` 요소의 가장 중요한 속성은 링크의 수신처를 나타내는 ```href``` 속성입니다.

링크 텍스트는 독자가 볼 수 있는 부분입니다.

링크 텍스트를 클릭하면 판독기가 지정된 URL 주소로 전송됩니다.

###### 예제 1

```html
<a href="https://devjiraynor.github.io/">Jiraynor`s blog</a>
```

기본적으로 링크는 모든 브라우저에 다음과 같이 표시됩니다.

+ 방문하지 않은 링크에 밑줄이 그어져 파란색으로 표시됩니다.
+ 방문한 링크는 밑줄이 그어져 보라색입니다.
+ 활성 링크에 밑줄이 그어져 빨간색으로 표시됩니다.

{: .box-note}
**Tip:** 링크는 물론 CSS로 스타일링할 수 있어 다른 모습을 볼 수 있습니다.

