---
layout: post
title: HTML 22. 파일 경로 (File paths)
subtitle: 파일 경로는 웹 사이트의 폴더 구조에서 파일의 위치를 설명합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/A2En24etv9Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<a href="https://youtu.be/A2En24etv9Y" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 22. 파일 경로 (File paths)</a>
<br>
<br>

# HTML 파일 경로

## HTML 파일 경로

파일 경로는 웹 사이트의 폴더 구조에서 파일의 위치를 설명합니다.

파일 경로는 다음과 같은 외부 파일에 링크할 때 사용됩니다.

+ 웹 페이지
+ 이미지들
+ 스타일 시트
+ 자바스크립트

## 절대 경로

절대 파일 경로는 파일의 전체 URL입니다.

###### 예제 1

```html
<img src="https://www.w3schools.com/images/picture.jpg" alt="Mountain">
```

## 상대 경로

상대 파일 경로는 현재 페이지에 상대적인 파일을 가리킵니다.

다음 예제에서는 파일 경로가 현재 웹 루트에 있는 이미지 폴더의 파일을 가리킵니다.

###### 예제 2

```html
<img src="/images/picture.jpg" alt="Mountain">
```

다음 예제에서는 파일 경로가 현재 폴더에 있는 이미지 폴더의 파일을 가리킵니다.

###### 예제 3

```html
<img src="images/picture.jpg" alt="Mountain">
```

다음 예제에서는 파일 경로가 현재 폴더에서 한 단계 위에 있는 이미지 폴더의 파일을 가리킵니다.

###### 예제 4

```html
<img src="../images/picture.jpg" alt="Mountain">
```

## 최선의 선택

가능한 경우 상대 파일 경로를 사용하는 것이 좋습니다.

상대 파일 경로를 사용할 때 웹 페이지는 현재 기본 URL에 바인딩되지 않습니다. 모든 링크는 현재 공용 도메인 및 미래의 공용 도메인뿐만 아니라 자신의 컴퓨터(로컬 호스트)에서도 작동합니다.
