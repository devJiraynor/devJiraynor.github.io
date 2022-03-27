---
layout: post
title: HTML 41. 캔버스 (Canvas)
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

<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;">
</canvas>

###### 예제 1

```html
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;">
</canvas>
```

## Javascript 추가

직사각형 캔버스 영역을 작성한 후 그림을 그릴 JavaScript를 추가해야 합니다.

다음은 몇 가지 예입니다.

#### 선 그리기

<canvas id="myCanvas1" width="200" height="100" style="border:1px solid #000000;">
</canvas>

<script>
var c = document.getElementById("myCanvas1");
var ctx = c.getContext("2d");
ctx.moveTo(0, 0);
ctx.lineTo(200, 100);
ctx.stroke();
</script>

###### 예제 2

```html
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.moveTo(0, 0);
ctx.lineTo(200, 100);
ctx.stroke();
</script>
```

#### 원 그리기

<canvas id="myCanvas2" width="200" height="100" style="border:1px solid #000000;">
</canvas>

<script>
var c = document.getElementById("myCanvas2");
var ctx = c.getContext("2d");
ctx.beginPath();
ctx.arc(95, 50, 40, 0, 2 * Math.PI);
ctx.stroke();
</script>

###### 예제 3

```html
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.beginPath();
ctx.arc(95, 50, 40, 0, 2 * Math.PI);
ctx.stroke();
</script>
```

#### 텍스트 그리기

<canvas id="myCanvas3" width="200" height="100" style="border:1px solid #000000;">
</canvas>

<script>
var c = document.getElementById("myCanvas3");
var ctx = c.getContext("2d");
ctx.font = "30px Arial";
ctx.fillText("Hello World", 10, 50);
</script>

###### 예제 4

```html
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.font = "30px Arial";
ctx.fillText("Hello World", 10, 50);
</script>
```

#### 스트로크 텍스트

<canvas id="myCanvas4" width="200" height="100" style="border:1px solid #000000;">
</canvas>

<script>
var c = document.getElementById("myCanvas4");
var ctx = c.getContext("2d");
ctx.font = "30px Arial";
ctx.strokeText("Hello World", 10, 50);
</script>

###### 예제 5

```html
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.font = "30px Arial";
ctx.strokeText("Hello World", 10, 50);
</script>
```

#### 선형 그라데이션 그리기

<canvas id="myCanvas5" width="200" height="100" style="border:1px solid #000000;">
</canvas>

<script>
var c = document.getElementById("myCanvas5");
var ctx = c.getContext("2d");

var grd = ctx.createLinearGradient(0, 0, 200, 0);
grd.addColorStop(0, "red");
grd.addColorStop(1, "white");

ctx.fillStyle = grd;
ctx.fillRect(10, 10, 150, 80);
</script>

###### 예제 6

```html
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");

// 그라데이션 생성
var grd = ctx.createLinearGradient(0, 0, 200, 0);
grd.addColorStop(0, "red");
grd.addColorStop(1, "white");

// 그라데이션 채우기
ctx.fillStyle = grd;
ctx.fillRect(10, 10, 150, 80);
</script>
```

#### 원형 그라데이션 그리기

<canvas id="myCanvas6" width="200" height="100" style="border:1px solid #000000;">
</canvas>

<script>
var c = document.getElementById("myCanvas6");
var ctx = c.getContext("2d");

var grd = ctx.createRadialGradient(75, 50, 5, 90, 60, 100);
grd.addColorStop(0, "red");
grd.addColorStop(1, "white");

ctx.fillStyle = grd;
ctx.fillRect(10, 10, 150, 80);
</script>

###### 예제 7

```html
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");

// 그라데이션 생성
var grd = ctx.createRadialGradient(75, 50, 5, 90, 60, 100);
grd.addColorStop(0, "red");
grd.addColorStop(1, "white");

// 그라데이션 채우기
ctx.fillStyle = grd;
ctx.fillRect(10, 10, 150, 80);
</script>
```

###### 예제 8 - 이미지 그리기

```html
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
var img = document.getElementById("scream");
ctx.drawImage(img, 10, 10);
</script>
```
