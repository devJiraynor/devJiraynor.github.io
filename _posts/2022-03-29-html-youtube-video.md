---
layout: post
title: HTML 46. 유튜브 (YouTube Video)
subtitle: HTML로 동영상을 재생하는 가장 쉬운 방법은 유튜브를 사용하는 것입니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<a href="https://youtu.be/eLn3PkL4pBM" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 46. 유튜브 (YouTube Video) 영상 보러가기</a>
<br>
<br>

# HTML 유튜브 (YouTube Video)

## 비디오 포맷에 어려움을 겪고 계십니까?

비디오를 다른 형식으로 변환하는 것은 어렵고 시간이 많이 걸릴 수 있습니다.

보다 쉬운 해결책은 YouTube가 웹 페이지에서 동영상을 재생하도록 하는 것입니다.

## YouTube 비디오 ID

YouTube는 비디오를 저장(또는 재생)할 때 ID(tgbNymZ7vqY 등)를 표시합니다.

이 ID를 사용하여 HTML 코드로 동영상을 참조할 수 있습니다.

## HTML로 유튜브 비디오 재생

Web 페이지에서 비디오를 재생하려면 다음의 순서 대로 진행합니다.

+ YouTube에 동영상 업로드합니다.
+ 비디오 ID를 메모해둡니다.
+ 웹 페이지에서 ```<iframe>``` 요소를 정의합니다.
+ ```src``` 속성이 비디오 URL을 가리키도록 합니다.
+ ```width``` 및 ```height``` 속성을 사용하여 플레이어의 치수 지정합니다.
+ URL에 파라미터를 추가합니다.

###### 예제 1

```html
<iframe width="420" height="315"
src="https://www.youtube.com/embed/tgbNymZ7vqY">
</iframe>
```

## YouTube 자동 재생 + 음소거

youtube URL에 ```autoplay=1```을 추가해, 사용자가 페이지를 방문했을 때에 자동적으로 동영상 재생을 개시할 수 있습니다만, 동영상 자동 재생은 방문자들이 선호하지 않습니다.

{:. box-note}
**Note:** 대부분의 경우 크롬 브라우저는 자동 재생을 지원하지 않습니다. 단, 음소거 자동 재생은 항상 허용됩니다.

```autoplay=1``` 뒤에 ```mute=1```을 추가하여 비디오의 자동 재생을 시작합니다(단, 음소거).

###### 예제 2

```html
<iframe width="420" height="315"
src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=1&mute=1">
</iframe>
```

## YouTube 재생 목록

재생할 비디오의 쉼표로 구분해서 재생목록을 만들수 있습니다.

## YouTube 반복

비디오를 반복하려면 ```loop=1```을 추가합니다.

값 0(기본값): 1회만 재생됩니다.

값 1: 계속 반복됩니다.

###### 예제 3

```html
<iframe width="420" height="315"
src="https://www.youtube.com/embed/tgbNymZ7vqY?playlist=tgbNymZ7vqY&loop=1">
</iframe>
```

## YouTube 제어

비디오 플레이어에 컨트롤러를 표시하지 않으려면 ```controls=0```을 추가합니다.

값 0: 플레이어 컨트롤러가 표시되지 않습니다.

값 1(디폴트): 플레이어가 디스플레이를 제어합니다.

###### 예제 4

```html
<iframe width="420" height="315"
src="https://www.youtube.com/embed/tgbNymZ7vqY?controls=0">
</iframe>
```
