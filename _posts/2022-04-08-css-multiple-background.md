---
layout: post
title: CSS 46. 다중 배경 (Multiple Backgrounds)
subtitle: 하나의 요소에 여러 배경 이미지를 추가하는 방법에 대해 알아봅니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

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

## 여러 배경 이미지의 크기 정의

또한 여러 배경으로 작업할 때 ```background-size``` 속성에는 여러 개의 값(쉼표로 구분된 목록 사용)이 허용됩니다.

다음 예에서는 세 개의 배경 이미지가 지정되었으며 각 이미지에 대해 다른 배경 크기 값이 지정되어 있습니다.

###### 예제 5

```css
#example1 {
  background: url(img_tree.gif) left top no-repeat, url(img_flwr.gif) right bottom no-repeat, url(paper.gif) left top repeat;
  background-size: 50px, 130px, auto;
}
```

## 전체 크기 배경 이미지

전체 브라우저 창을 항상 포함하는 웹 사이트에 배경 이미지를 표시하려고 합니다.

요구 사항은 다음과 같습니다.

+ 전체 페이지를 이미지로 채우기(공백 없음)
+ 필요에 따라 이미지 확장
+ 이미지의 페이지 중앙 위치
+ 스크롤 막대를 생성하지 않음

다음 예제에서는 이 작업을 수행하는 방법을 보여 줍니다. ```<html>``` 요소를 사용합니다.(```<html>``` 요소는 항상 브라우저 창의 높이 이상임). 그런 다음 고정되고 중앙에 있는 배경을 설정합니다. 그런 다음 ```background-size``` 속성을 사용하여 크기를 조정합니다.

###### 예제 6

```css
html {
  background: url(img_man.jpg) no-repeat center fixed;
  background-size: cover;
}
```

## hero 이미지

또한 ```<div>```의 다른 배경 속성을 사용하여 hero 이미지(텍스트가 있는 큰 이미지)를 만들고 원하는 위치에 배치할 수 있습니다.
  
###### 예제 7

```css
.hero-image {
  background: url(img_man.jpg) no-repeat center;
  background-size: cover;
  height: 500px;
  position: relative;
}
```

## background-origin 속성

```background-origin``` 속성은 배경 이미지가 위치할 위치를 지정합니다.

속성은 세 가지 다른 값을 사용합니다.

+ ```border-box``` - 배경 이미지는 테두리의 왼쪽 상단 모서리에서 시작됩니다.
+ ```padding-box``` - (기본값) 배경 이미지는 패딩 모서리의 왼쪽 상단 모서리에서 시작됩니다.
+ ```content-box``` - 배경 이미지는 내용의 왼쪽 상단 모서리에서 시작합니다.

###### 예제 8

```css
#example1 {
  border: 10px solid black;
  padding: 35px;
  background: url(img_flwr.gif);
  background-repeat: no-repeat;
  background-origin: content-box;
}
```

## background-clip 속성

```background-clip``` 속성은 배경의 그림 영역을 지정합니다.

속성은 세 가지 다른 값을 사용합니다.

```border-box``` - (기본값) 배경은 테두리의 바깥쪽 가장자리에 그려집니다.
```padding-box``` - 배경은 패딩의 바깥쪽 가장자리에 그려집니다.
```content-box``` - 배경은 content box 내에서 그려집니다.

###### 예제 9

```css
#example1 {
  border: 10px dotted black;
  padding: 35px;
  background: yellow;
  background-clip: content-box;
}
```
