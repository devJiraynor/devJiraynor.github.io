---
layout: post
title: CSS 46. 다중 배경 (Multiple Backgrounds)
subtitle: 하나의 요소에 여러 배경 이미지를 추가하는 방법에 대해 알아봅니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
--

# CSS 다중 배경 (Multiple Backgrounds)

## 다중 배경

CSS를 사용하면 ```background-image``` 속성을 통해 요소에 대한 여러 배경 이미지를 추가할 수 있습니다.

서로 다른 배경 이미지는 쉼표로 구분되며 이미지가 서로 겹쳐져 첫 번째 이미지가 뷰어에 가장 가깝습니다.

###### 예제 1

```css
#example1 {
  background-image: url(img_flwr.gif), url(paper.gif);
  background-position: right bottom, left top;
  background-repeat: no-repeat, repeat;
}
```

여러 배경 이미지는 개별 배경 속성(위 참조) 또는 ```background``` 축약 속성을 사용하여 지정할 수 있습니다.

###### 예제 2

```css
#example1 {
  background: url(img_flwr.gif) right bottom no-repeat, url(paper.gif) left top repeat;
}
```

## 배경 크기

```background-size``` 속성을 사용하여 배경 이미지의 크기를 지정할 수 있습니다.

크기는 길이, 백분율 또는 포함 또는 두 가지 키워드 중 하나를 사용하여 지정할 수 있습니다.

###### 예제 3

```css
#div1 {
  background: url(img_flower.jpg);
  background-size: 100px 80px;
  background-repeat: no-repeat;
}
```

```background-size```에 대해 가능한 두 가지 다른 값은 ```container``` 및 ```cover```입니다.

```contain``` 키워드는 배경 이미지를 가능한 한 크게 조정합니다(단, 가로와 세로 모두 내용 영역 내에 들어가야 함). 따라서 배경 이미지와 배경 위치 지정 영역의 비율에 따라 배경 이미지에 포함되지 않는 일부 영역이 있을 수 있습니다.

```cover``` 키워드는 내용 영역이 배경 이미지에 의해 완전히 가려지도록 배경 이미지의 크기를 조정합니다(폭과 높이가 모두 내용 영역과 같거나 초과됨). 따라서 배경 이미지의 일부 부분이 배경 위치 지정 영역에서 보이지 않을 수 있습니다.

다음 예에서는 ```contain``` 및 ```cover```의 사용을 보여 줍니다.

###### 예제 4

```css
#div1 {
  background: url(img_flower.jpg);
  background-size: contain;
  background-repeat: no-repeat;
}

#div2 {
  background: url(img_flower.jpg);
  background-size: cover;
  background-repeat: no-repeat;
}
```
