---
layout: post
title: CSS 35. 이미지 스프라이트 (Image Sprites)
subtitle: 이미지 스프라이트는 단일 이미지에 삽입된 이미지의 모음입니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 이미지 스프라이트

## 이미지 스프라이트

이미지 스프라이트는 단일 이미지에 삽입된 이미지의 모음입니다.

이미지가 많은 웹 페이지는 로드하는 데 오랜 시간이 걸릴 수 있으며 여러 서버 요청을 생성합니다.

이미지 스프라이트를 사용하면 서버 요청 수가 줄어들고 대역폭이 절약됩니다.

## 이미지 스프라이트 - 간단한 예제

세 개의 개별 이미지를 사용하는 대신 이 단일 이미지("img_navsprites.gif")를 사용합니다.

CSS를 사용하면 필요한 부분만 이미지를 보여줄 수 있습니다.

다음 예제에서 CSS는 "img_navsprites.gif" 이미지의 어느 부분을 표시할지 지정합니다.

###### 예제 1

```css
#home {
  width: 46px;
  height: 44px;
  background: url(img_navsprites.gif) 0 0;
}
```

**예제 설명:**

+ ```<img id="home" src="img_trans.gif">``` - src 속성은 비워 둘 수 없으므로 작은 투명 이미지만 정의합니다. 표시된 이미지는 CSS에서 지정한 배경 이미지가 됩니다.
+ ```width: 46px; height: 44px;``` - 사용할 이미지 부분의 크기를 정의합니다.
+ ```background: url(img_navsprites.gif) 0 0;``` - 배경 이미지와 해당 위치를 정의합니다(왼쪽 0px, 위쪽 0px).

## 이미지 스프라이트 - 네비게이션 리스트 생성

스프라이트 이미지("img_navsprites.gif")를 사용하여 네비게이션 리스트를 생성하려고 합니다.

HTML 목록이 링크가 될 수 있고 배경 이미지를 지원하므로 HTML 리스트를 사용합니다.

###### 예제 2

```css
#navlist {
  position: relative;
}

#navlist li {
  margin: 0;
  padding: 0;
  list-style: none;
  position: absolute;
  top: 0;
}

#navlist li, #navlist a {
  height: 44px;
  display: block;
}

#home {
  left: 0px;
  width: 46px;
  background: url('img_navsprites.gif') 0 0;
}

#prev {
  left: 63px;
  width: 43px;
  background: url('img_navsprites.gif') -47px 0;
}

#next {
  left: 129px;
  width: 43px;
  background: url('img_navsprites.gif') -91px 0;
}
```

**예제 설명:**

+ ```#navlist {position:relative;}``` - ```position```은 그 안에 절대적인 위치를 지정할 수 있도록 상대적인 위치로 설정됩니다.
+ ```#navlist li {margin:0;padding:0;list-style:none;position:absolute;top:0;}``` - ```margin``` 및 ```padding```이 0으로 설정되고 리스트 스타일이 제거되며 모든 리스트 항목이 절대 위치에 놓입니다.
+ ```#navlist li, #navlist a {height:44px;display:block;}``` - 모든 이미지의 높이를 44px로 맞춥니다.

