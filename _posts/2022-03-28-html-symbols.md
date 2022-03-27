---
layout: post
title: HTML 41. 심볼 (Symbols)
subtitle: HTML canvas 요소는 웹 페이지에 그래픽을 그리기 위해 사용됩니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML canvas 그래픽

HTML ```<canvas>``` 요소는 웹 페이지에 그래픽을 그리기 위해 사용됩니다.

빨간색 직사각형, 그라데이션 직사각형, 다색 직사각형 및 다색 텍스트의 네 가지 요소가 표시됩니다.

## HTML canvas란?

HTML ```<canvas>``` 요소는 JavaScript를 통해 그래픽을 즉시 그리기 위해 사용됩니다.

```<canvas>``` 요소는 그래픽용 컨테이너일 뿐입니다. 실제로 그래픽을 그리려면 JavaScript를 사용해야 합니다.

캔버스에는 경로, 상자, 원, 텍스트 및 이미지 추가를 위한 여러 가지 방법이 있습니다.

## 지원하는 브라우저

표의 숫자는 ```<canvas>``` 요소를 완전히 지원하는 최소 브라우저 버전을 나타냅니다.

| 브라우저 | 구글 Chrome | 마이크로소프트 Edge | Firefox | Safari | Opera |
| 버전 | 4.0 | 9.0 | 2.0 | 3.1 | 9.0 |

## Canvas 예제

캔버스는 HTML 페이지의 직사각형 영역입니다. 기본적으로 캔버스에는 테두리와 내용이 없습니다.

코드는 다음과 같습니다.

```html
<canvas id="myCanvas" width="200" height="100"></canvas>
```

{: .box-note}
**Note:** 항상 ```id``` 속성(스크립트에서 참조)과 ```width``` 및 ```height``` 속성을 지정하여 캔버스의 크기를 정의하십시오. 테두리를 추가하려면 ```style``` 속성을 사용합니다.

다음은 기본적인 빈 캔버스의 예를 나타냅니다.

<canvas id="myCanvas" width="200" height="100"></canvas>
