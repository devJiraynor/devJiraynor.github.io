---
layout: post
title: HTML 14. 파비콘 (Favicon)
subtitle: favicon은 브라우저 탭의 페이지 제목 옆에 표시되는 작은 이미지입니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/_MuY7JWFM8o" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<a href="https://youtu.be/_MuY7JWFM8o" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 14. 파비콘 (Favicon)</a>
<br>
<br>

# HTML 파비콘

## HTML에서 Favicon을 추가하는 방법

마음에 드는 이미지를 마음에 드는 아이콘으로 사용할 수 있습니다. https://favicon.cc 와 같은 사이트에서 자신만의 favicon을 만들 수도 있습니다.

{: .box-note}
**Tip:** favicon은 작은 이미지이기 때문에 콘트라스트가 높은 심플한 이미지여야 합니다.

브라우저 탭의 페이지 제목 왼쪽에 다음과 같이 favicon 이미지가 표시됩니다.

![html_favicon_01](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_favicon_01.PNG?raw=true)

웹 사이트에 favicon을 추가하려면 웹 서버의 루트 디렉토리에 favicon 이미지를 저장하거나 images라는 이름의 루트 디렉토리에 폴더를 만들고 이 폴더에 favicon 이미지를 저장합니다. favicon 이미지의 일반적인 이름은 "favicon.ico"입니다.

다음으로 ```<title>``` 요소 뒤에 다음과 같이 ```<link>``` 요소를 "index.html" 파일에 추가합니다.

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Page Title</title>
  <link rel="icon" type="image/x-icon" href="/images/favicon.ico">
</head>
<body>

<h1>표제입니다.</h1>
<p>문단입니다.</p>

</body>
</html>
```

이제 "index.html" 파일을 저장하고 브라우저에 다시 로드합니다. 브라우저 탭에 페이지 제목 왼쪽에 즐겨찾기 이미지가 표시됩니다.

## Favicon 파일 형식 지원

다음 표에 favicon 이미지의 파일 형식 지원을 나타냅니다.

| 브라우저 | ICO | PNG | GIF | JPEG | SVG |
| Edge | 가능 | 가능 | 가능 | 가능 | 가능 |
| Chrome | 가능 | 가능 | 가능 | 가능 | 가능 |
| Firefox | 가능 | 가능 | 가능 | 가능 | 가능 |
| Opera | 가능 | 가능 | 가능 | 가능 | 가능 |
| Safari | 가능 | 가능 | 가능 | 가능 | 가능 |

## Summary

+ HTML ```<link>``` 요소를 사용하여 favicon 삽입
