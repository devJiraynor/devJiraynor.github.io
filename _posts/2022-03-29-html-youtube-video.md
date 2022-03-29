---
layout: post
title: HTML 46. 유튜브 (YouTube Video)
subtitle: HTML로 동영상을 재생하는 가장 쉬운 방법은 유튜브를 사용하는 것입니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

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

