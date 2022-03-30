---
layout: post
title: HTML 13-1. 이미지 맵 (Image - map)
subtitle: HTML 이미지 맵을 사용하면 이미지에 클릭 가능한 영역을 만들 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 이미지 맵

## 이미지 맵

HTML ```<map>``` 태그는 이미지 맵을 정의합니다. 이미지 맵은 클릭 가능한 영역이 있는 이미지입니다. 영역은 하나 이상의 ```<area>``` 태그로 정의됩니다.

다음 이미지에서 컴퓨터, 전화기 또는 커피잔을 클릭해 보겠습니다.

![html-image-maps-01](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_image_map_01.jpg?raw=true)

###### 예제 1

```html
<img src="html_image_map_01.jpg" alt="Workplace" usemap="#workmap">

<map name="workmap">
  <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.html">
  <area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.html">
  <area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.html">
</map>
```

## 작동 방식

이미지 맵의 개념은 클릭하는 이미지의 위치에 따라 다른 액션을 수행할 수 있어야 한다는 것입니다.

이미지 맵을 작성하려면 이미지와 클릭 가능한 영역을 설명하는 HTML 코드가 필요합니다.

## 이미지

이미지는 ```<img>``` 태그를 사용하여 삽입됩니다. 다른 이미지와의 유일한 차이점은 ```usemap``` 속성을 추가해야 한다는 것입니다.

```html
<img src="html_image_map_01.jpg" alt="Workplace" usemap="#workmap">
```

```usemap``` 값은 해시 태그 ```#``` 에서 시작하여 이미지 맵의 이름으로 시작합니다.이 값은 이미지와 이미지 맵의 관계를 작성하기 위해 사용됩니다.

{: .box-note}
**Tip:** 어떤 이미지라도 이미지 맵으로 사용할 수 있습니다!

## 이미지 맵 작성

다음으로 ```<map>``` 요소를 추가합니다.

```<map>``` 요소는 이미지 맵 작성에 사용되며 필요한 ```name``` 속성을 사용하여 이미지에 링크됩니다.

```html
<map name="workmap">
```

```name``` 속성은 ```<img>``` 의 ```usemap``` 속성과 같은 값을 가져야 합니다.

## 영역

다음은 클릭 가능한 영역을 추가합니다.

클릭 가능한 영역은 ```<area>``` 요소를 사용하여 정의됩니다.

##### 모양 (Shape)

클릭 가능한 영역의 모양을 정의해야 하며 다음 값 중 하나를 선택할 수 있습니다.

+ ```rect``` - 직사각형 영역을 정의합니다.
+ ```circle``` - 원형 영역을 정의합니다.
+ ```poly``` - 다각형 영역을 정의합니다.
+ ```default``` - 지역 전체를 정의합니다.

또한 클릭 가능한 영역을 이미지에 배치할 수 있도록 몇 가지 좌표를 정의해야 합니다.

##### Shape="rect"

```shape="rect"``` 좌표는 쌍으로 제공되며, 하나는 x축에, 다른 하나는 y축에 있습니다.

따라서 좌표 ```34,44``` 는 왼쪽 여백에서 34픽셀, 위쪽에서 44픽셀입니다.

![html-image-maps-02](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_image_map_02.PNG?raw=true)

좌표 ```270,350``` 은 왼쪽 여백에서 270픽셀, 위쪽에서 350픽셀에 위치합니다.

![html-image-maps-03](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_image_map_03.PNG?raw=true)

이제 클릭 가능한 직사각형 영역을 만들 수 있는 충분한 데이터가 있습니다.

```html
<area shape="rect" coords="34, 44, 270, 350" href="computer.htm">
```

이 영역은 클릭할 수 있게 되어 사용자를 "computer.html" 페이지로 보냅니다.

![html-image-maps-04](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_image_map_04.PNG?raw=true)

##### Shape="circle"

원 영역을 추가하려면 먼저 원 중심 좌표를 찾습니다.

```337, 300```

![html-image-maps-05](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_image_map_05.PNG?raw=true)

그런 다음 원의 반지름을 지정합니다.

```44``` 픽셀

![html-image-maps-06](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_image_map_06.PNG?raw=true)

이제 클릭 가능한 원형 영역을 만들 수 있는 충분한 데이터가 있습니다.

```html
<area shape="circle" coords="337, 300, 44" href="coffee.htm">
```

이 영역은 클릭할 수 있게 되어 사용자를 "coffee.html" 페이지로 보냅니다.

![html-image-maps-07](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_image_map_07.PNG?raw=true)

##### Shape="poly"

```shape="poly"``` 에는 직선(폴리곤)으로 형성된 모양을 만드는 여러 개의 좌표 점이 포함되어 있습니다.

모든 모양을 만드는 데 사용할 수 있습니다.

아래 이미지의 크루아상을 클릭 가능한 링크로 만들려면 어떻게 해야 할까요?

![html-image-maps-08](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_image_map_08.jpg?raw=true)

크로와상의 모든 모서리에 대한 x 및 y 좌표를 찾아야 합니다.

![html-image-maps-09](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_image_map_09.PNG?raw=true)

좌표는 x축과 y축에 각각 하나씩 쌍으로 제공됩니다.

```html
<area shape="poly" coords="140,121,181,116,204,160,204,222,191,270,140,329,85,355,58,352,37,322,40,259,103,161,128,147" href="croissant.htm">
```

이 영역은 클릭할 수 있게 되어 사용자를 "croissant.htm" 페이지로 보냅니다.

![html-image-maps-10](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_image_map_10.PNG?raw=true)

## 이미지 맵과 JavaScript

클릭 가능한 영역은 JavaScript 함수를 트리거할 수도 있습니다.

```click``` 이벤트를 ```<area>``` 요소에 추가하여 JavaScript 함수를 실행합니다.

###### 예제 (영역을 클릭했을 때 onclick 속성을 사용하여 JavaScript 함수를 실행합니다.)

```html
<map name="workmap">
  <area shape="circle" coords="337,300,44" href="coffee.html" onclick="myFunction()">
</map>

<script>
function myFunction() {
  alert("You clicked the coffee cup!");
}
</script>
```

## Summary

+ HTML ```<map>``` 요소를 사용하여 이미지 맵을 정의합니다.
+ HTML ```<area>``` 요소를 사용하여 이미지 맵에서 클릭 가능한 영역을 정의합니다.
+ 이미지 맵을 가리키려면 ```<img>``` 요소의 HTML ```usemap``` 속성을 사용합니다.

