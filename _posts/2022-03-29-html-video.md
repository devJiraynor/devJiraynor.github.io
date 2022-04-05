---
layout: post
title: HTML 44. 비디오 (Video)
subtitle: HTML video 요소는 웹 페이지에 비디오를 표시하기 위해 사용됩니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<a href="https://youtu.be/I2JvmOHI3Ho" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 44. 비디오 (Video) 영상 보러가기</a>
<br>
<br>

# HTML 비디오

## HTML ```<video>``` 요소

HTML 로 비디오를 표시하려면 ```<video>``` 요소를 사용합니다.

###### 예제 1

```html
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
</video>
```

## 구조

```controls``` 속성은 재생, 일시 중지 및 볼륨과 같은 비디오 컨트롤을 추가합니다.

항상 ```width``` 및 ```height``` 속성을 포함하는 것이 좋습니다. 높이와 폭을 설정하지 않으면 비디오 로드 중에 페이지가 깜박일 수 있습니다.

```<source>``` 요소에서는 브라우저가 선택할 수 있는 대체 비디오파일을 지정할 수 있습니다. 브라우저는 처음 인식된 형식을 사용합니다.

```<video>``` 태그와 ```</video>``` 태그 사이의 텍스트는 ```<video>``` 요소를 지원하지 않는 브라우저에서만 표시됩니다.

## HTML ```<video>``` 자동 재생

비디오를 자동적으로 재생되게 하려면 ```autoplay``` 속성을 사용합니다.

###### 예제 2

```html
<video width="320" height="240" autoplay>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
</video>
```

{: .box-note}
**Note:** 대부분의 경우 크롬 브라우저는 자동 재생을 지원하지 않습니다. 단, 음소거 자동 재생은 항상 허용됩니다.

```autoplay``` 후 ```muted```를 추가하여 비디오 재생을 자동으로 시작합니다(단, 음소거).

###### 예제 3

```html
<video width="320" height="240" autoplay muted>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
</video>
```

## 지원 브라우저

표의 숫자는 ```<video>``` 요소를 완전히 지원하는 최소 브라우저 버전을 나타냅니다.

| 브라우저 | 구글 Chrome | 마이크로소프트 Edge | Firefox | Safari | Opera |
| 버전 | 4.0 | 9.0 | 3.5 | 4.0 | 10.5 |

## HTML 비디오 형식

MP4, WebM 및 Ogg의 3가지 비디오 형식이 지원됩니다. 다양한 포맷에 대한 브라우저 지원은 다음과 같습니다.

| 브라우저 | MP4 |  WebM | Ogg |
| Edge | Yes | Yes | Yes |
| Chrome | Yes | Yes | Yes |
| Firefox | Yes | Yes | Yes |
| Safari | Yes | Yes | No |
| Opera | Yes | Yes | Yes |

## HTML 비디오 - 미디어 유형

| 파일 형식 | 미디어 타입 |
| MP4 | video/mp4 |
| WebM | video/webm |
| Ogg | video/ogg |

## HTML 비디오 - 메서드, 속성 및 이벤트

HTML DOM은 ```<video>``` 요소의 메서드, 속성 및 이벤트를 정의합니다.

이를 통해 비디오의 로드, 재생, 일시정지, 및 기간과 볼륨을 설정할 수 있습니다.

또, 비디오의 재생 시작, 일시 정지등을 통제하는 DOM 이벤트도 있습니다.
  
###### 예제 4

```html
<body> 

<div style="text-align:center"> 
  <button onclick="playPause()">Play/Pause</button> 
  <button onclick="makeBig()">Big</button>
  <button onclick="makeSmall()">Small</button>
  <button onclick="makeNormal()">Normal</button>
  <br><br>
  <video id="video1" width="420">
    <source src="mov_bbb.mp4" type="video/mp4">
    <source src="mov_bbb.ogg" type="video/ogg">
  </video>
</div> 

<script> 
var myVideo = document.getElementById("video1"); 

function playPause() { 
  if (myVideo.paused) 
    myVideo.play(); 
  else 
    myVideo.pause(); 
} 

function makeBig() { 
    myVideo.width = 560; 
} 

function makeSmall() { 
    myVideo.width = 320; 
} 

function makeNormal() { 
    myVideo.width = 420; 
} 
</script> 

<p>Video courtesy of <a href="https://www.bigbuckbunny.org/" target="_blank">Big Buck Bunny</a>.</p>
```
