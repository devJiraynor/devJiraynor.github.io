---
layout: post
title: CSS 12. 박스 모델 (Box Model)
subtitle: 모든 HTML 요소는 상자로 간주할 수 있습니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 박스 모델

## 박스 모델

CSS에서 "박스 모델"이라는 용어는 설계와 레이아웃에 대해 말할 때 사용됩니다.

CSS 박스 모델은 기본적으로 모든 HTML 요소를 감싸는 상자입니다. 여백, 테두리, 패딩 및 실제 콘텐츠로 구성됩니다. 아래 그림은 박스 모델을 나타내고 있습니다.

<img src="https://raw.githubusercontent.com/devJiraynor/devJiraynor.github.io/master/assets/img/css/css_box_model_01.PNG">

+ Content - 텍스트와 이미지가 표시되는 상자의 내용
+ Padding - 테두리와 컨텐츠 사이의 공간
+ Border - 패딩과 컨텐츠를 둘러싸고 있는 테두리
+ Margin - 테두리 바깥의 공간

상자 모델을 사용하면 요소 주위에 경계를 추가하고 요소 간의 공간을 정의할 수 있습니다.

###### 예제 1

```css
div {
  width: 300px;
  border: 15px solid green;
  padding: 50px;
  margin: 20px;
}
```

## 요소의 높이와 너비

모든 브라우저에서 요소의 너비와 높이를 올바르게 설정하려면 상자 모델에 대해 정확히 이해해야 합니다.

{: .box-note}
**중요:** CSS를 사용하여 요소의 너비와 높이 속성을 설정할 때는 **콘텐츠 영역**의 너비와 높이만 설정합니다. 요소의 전체 크기를 계산하려면 패딩, 테두리 및 여백도 추가해야 합니다.

###### 예제 2

```css
div {
  width: 320px;
  padding: 10px;
  border: 5px solid gray;
  margin: 0;
}
```

너비 계산 결과:

{: box-warning}
320px(width)<br>+ 20px (left + right padding)<br>+ 10px(left + right border)<br>+ 0px(left + right margin)<br>= **350px**

요소의 총 너비는 다음과 같이 계산해야 합니다.

전체 요소 폭 = 너비 + 왼쪽 패딩 + 오른쪽 패딩 + 왼쪽 테두리 + 오른쪽 테두리 + 왼쪽 마진 + 오른쪽 마진

요소의 총 높이는 다음과 같이 계산해야 합니다.

총 요소 높이 = 높이 + 상단 패딩 + 하단 패딩 + 상단 테두리 + 상단 테두리 + 상단 여마진 + 하단 마진

