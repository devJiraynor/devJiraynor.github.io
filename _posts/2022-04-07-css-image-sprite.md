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

이제 각 특정 부분에 대한 위치와 스타일을 시작합니다.

+ ```#home {left:0px;width:46px;}``` - 왼쪽 끝에 위치하며, 이미지의 너비는 46px입니다.
+ ```#home {background:url(img_navsprites.gif) 0 0;}``` - 배경 이미지와 해당 위치를 정의합니다(왼쪽 0px, 위쪽 0px).
+ ```#prev {left:63px;width:43px;}``` - 시작점으로 부터 63px 오른쪽에 배치하고(#home width 46px + 항목 사이의 일부 여유 공간), 너비는 43px입니다.
+ ```#prev {background:url('img_navsprites.gif') -47px 0;}``` - 오른쪽에 배경 이미지 47px를 정의합니다(#home width 46px + 1px 구분선).
+ ```#next {left:129px;width:43px;}``` - 시작점으로 부터 129px 오른쪽에 배치(#prev 시작은 63px + #prev 너비 43px + 여유 공간), 너비는 43px입니다.
+ ```#next {background:url('img_navsprites.gif') -91px 0;}``` - 오른쪽에 배경 이미지 91px를 정의합니다(#home width 46px + 1px 구분선 + #prev 너비 43px + 1px 구분선).

## 이미지 스프라이트 - 호버 효과

이제 네비게이션 리스트에 호버 효과를 추가하려고 합니다.

{: .box-note}
**Tip:** ```:hover``` 셀렉터는 링크뿐만 아니라 모든 요소에 사용할 수 있습니다.

새 이미지("img_navsprites_hover.gif")에는 호버 효과에 사용할 세 개의 탐색 이미지와 세 개의 이미지가 포함되어 있습니다.

이것은 6개의 개별 파일이 아닌 하나의 단일 이미지이기 때문에 사용자가 이미지 위로 호버할 때 로드 지연이 없습니다.

호버 효과를 추가하기 위해 세 줄의 코드만 추가합니다.

###### 예제 3

```css
#home a:hover {
  background: url('img_navsprites_hover.gif') 0 -45px;
}

#prev a:hover {
  background: url('img_navsprites_hover.gif') -47px -45px;
}

#next a:hover {
  background: url('img_navsprites_hover.gif') -91px -45px;
}
```

예제 설명:

+ ```#home a:hover {background: url('img_navsprites_hover.gif') 0 -45px;}``` - 세 개의 호버 이미지에 대해 동일한 배경 위치를 지정합니다. 아래쪽으로 45px만 더 내려갑니다.
