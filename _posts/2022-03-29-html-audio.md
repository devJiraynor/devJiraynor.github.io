---
layout: post
title: HTML 45. 오디오 (Audio)
subtitle: HTML audio 요소는 웹 페이지에서 오디오파일을 재생하기 위해 사용됩니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 오디오

## HTML ```<audio>``` 요소

HTML로 오디오 파일을 재생하려면 ```<audio>``` 요소를 사용합니다.

###### 예제 1

```html
<audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
</audio>
```

## HTML 오디오 - 구조

```controls``` 속성은 재생, 일시 중지, 볼륨 등의 오디오 컨트롤을 추가합니다.

```<source>``` 요소에서는 브라우저가 선택할 수 있는 대체 오디오파일을 지정할 수 있습니다. 브라우저는 처음 인식된 형식을 사용합니다.

```<audio>``` 태그와 ```</audio>``` 태그 사이의 텍스트는 ```<audio>``` 요소를 지원하지 않는 브라우저에서만 표시됩니다.

## HTML ```<audio>``` 자동 재생

오디오 파일을 자동으로 시작하려면 ```autoplay``` 속성을 사용합니다.

###### 예제 2

```html
<audio controls autoplay>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
</audio>
```

{: .box-note}
**Note:** 대부분의 경우 크롬 브라우저는 자동 재생을 지원하지 않습니다. 단, 음소거 자동 재생은 항상 허용됩니다.

autoplay 후 muted를 추가하여 오디오 재생을 자동으로 시작합니다(단, 음소거).

###### 예제 3

```html
<audio controls autoplay muted>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
</audio>
```

## 지원 브라우저

표의 숫자는 ```<audio>``` 요소를 완전히 지원하는 최소 브라우저 버전을 나타냅니다.

| 브라우저 | 구글 Chrome | 마이크로소프트 Edge | Firefox | Safari | Opera |
| 버전 | 4.0 | 9.0 | 3.5 | 4.0 | 10.5 |

## HTML 오디오 형식

MP3, WAV 및 OGG의 3가지 오디오 형식이 지원됩니다. 다양한 포맷에 대한 브라우저 지원은 다음과 같습니다.

| 브라우저 | MP3 |  WAV | Ogg |
| Edge | Yes | Yes | Yes |
| Chrome | Yes | Yes | Yes |
| Firefox | Yes | Yes | Yes |
| Safari | Yes | Yes | No |
| Opera | Yes | Yes | Yes |

## HTML 오디오 - 미디어 유형

| 파일 형식 | 미디어 타입 |
| MP3 | audio/mpeg |
| Ogg | audio/ogg |
| WAV | audio/wav |

## HTML 오디오 - 메서드, 속성 및 이벤트

HTML DOM은 ```<audio>``` 요소의 메서드, 속성 및 이벤트를 정의합니다.

오디오 로드, 재생, 및 일시 정지를 할 수 있을 뿐만 아니라 기간과 음량을 설정할 수 있습니다.

또, 오디오의 재생 시작, 일시 정지등을 통제하는 DOM 이벤트도 있습니다.
