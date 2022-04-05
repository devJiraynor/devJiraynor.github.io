---
layout: post
title: HTML 10. 색상 (Colors)
subtitle: HTML 의 색상은 미리 정의된 색상 이름 또는 RGB, HEX, HSL, RGBA, 또는 HSLA 의 값으로 지정됩니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<a href="https://youtu.be/4B9rioqT9To" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 10. 색상 (Colors) 영상 보러가기</a>
<br>
<br>


# HTML 색상

## 색상 이름

HTML 에서는 다음의 색명을 사용해 색을 지정할 수 있습니다.

![html_color_01](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_colors_01.PNG?raw=true)

HTML은 [140개의 표준 색상 이름][140_standard_color]을 지원합니다.

[140_standard_color]: https://www.w3schools.com/colors/colors_names.asp "140가지 기본 색상"

## 배경 색상

HTML 요소의 배경색을 설정할 수 있습니다.

![html_color_02](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_colors_02.PNG?raw=true)

###### 예제 1

```html
<h1 style="background-color:DodgerBlue;">Hello World</h1>
<p style="background-color:Tomato;">
Lorem ipsum dolor sit amet, consectetuer adipiscing elit, 
sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. 
Ut wisi enim ad minim veniam, quis nostrud exerci tation 
ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.
</p>
```

## 텍스트 색상

텍스트 색상을 설정할 수 있습니다.

![html_color_03](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_colors_03.PNG?raw=true)

###### 예제 2

```html
<h1 style="color:Tomato;">Hello World</h1>
<p style="color:DodgerBlue;">
Lorem ipsum dolor sit amet, consectetuer adipiscing elit, 
sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
</p>
<p style="color:MediumSeaGreen;">
Ut wisi enim ad minim veniam, quis nostrud exerci tation 
ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.
</p>
```

## 테두리 색

테두리 색상을 설정할 수 있습니다.

![html_color_04](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_colors_04.PNG?raw=true)

###### 예제 3

```html
<h1 style="border:2px solid Tomato;">Hello World</h1>
<h1 style="border:2px solid DodgerBlue;">Hello World</h1>
<h1 style="border:2px solid Violet;">Hello World</h1>
```

## 색상 값

HTML에서는 RGB 값, HEX 값, HSL 값, RGBA 값 및 HSLA 값을 사용하여 색상을 지정할 수도 있습니다.

다음 3개의 <div> 요소에는 RGB, HEX 및 HSL 값이 설정된 배경색이 있습니다.
  
![html_color_05](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_colors_05.PNG?raw=true)
  
다음 2개의 <div> 요소에는 RGBA 및 HSLA 값을 사용하여 배경색이 설정되어 있습니다. 색상에 알파 채널이 추가됩니다(여기에서는 투과율이 50%입니다).
  
![html_color_06](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_colors_06.PNG?raw=true)
  
###### 예제 4
  
```html
<h1 style="background-color:rgb(255, 99, 71);">rgb(255, 99, 71)</h1>
<h1 style="background-color:#ff6347;">#ff6347</h1>
<h1 style="background-color:hsl(9, 100%, 64%);">hsl(9, 100%, 64%)</h1>

<h1 style="background-color:rgba(255, 99, 71, 0.5);">rgba(255, 99, 71, 0.5)</h1>
<h1 style="background-color:hsla(9, 100%, 64%, 0.5);">hsla(9, 100%, 64%, 0.5)</h1>
```
