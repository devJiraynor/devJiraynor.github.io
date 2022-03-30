---
layout: post
title: HTML 13-3. picture 요소
subtitle: HTML picture 요소에서는, 디바이스 또는 화면 사이즈에 따라 다른 화상을 표시할 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---
  
# HTML ```<picture>``` 요소
  
## HTML ```<picture>``` 요소
  
HTML ```<picture>``` 요소를 사용하면 웹 개발자는 이미지 리소스를 보다 유연하게 지정할 수 있습니다.

```<picture>``` 요소에는 1개 이상의 ```<source>``` 요소가 포함되어 있습니다. 각 요소는 ```srcset``` 속성을 통해 다른 이미지를 참조합니다. 이렇게 하면 브라우저가 현재 보기 또는 장치에 가장 적합한 이미지를 선택할 수 있습니다.

각 ```<source>``` 요소에는 이미지가 가장 적합한 시기를 정의하는 ```media``` 속성이 있습니다.
  
###### 예제 (화면 크기에 따라 다른 이미지 표시)
  
```html
<picture>
  <source media="(min-width: 650px)" srcset="img_food.jpg">
  <source media="(min-width: 465px)" srcset="img_car.jpg">
  <img src="img_girl.jpg">
</picture>
```

{: .box-note}
**Note:** 항상 ```<img>``` 요소를 ```<picture>``` 요소의 마지막 자 요소로 지정합니다. ```<img>``` 요소는 ```<picture>``` 요소를 지원하지 않는 브라우저 또는 ```<source>``` 태그가 모두 일치하지 않는 경우 사용됩니다.

## Picture 요소를 사용하는 경우

```<picture>``` 요소에는 주로 다음 두 가지 목적이 있습니다.
  
##### 대역폭

작은 화면이나 장치가 있는 경우 큰 이미지 파일을 로드할 필요가 없습니다. 브라우저는 일치하는 속성 값을 가진 첫 번째 ```<source>``` 요소를 사용하며 다음 요소 중 하나를 무시합니다.

##### 포맷 지원

일부 브라우저 또는 디바이스는 일부 이미지 형식을 지원하지 않을 수 있습니다. ```<picture>``` 요소를 사용하면 모든 형식의 이미지를 추가할 수 있으며 브라우저는 인식되는 첫 번째 형식을 사용하며 다음 요소 중 하나를 무시합니다.

###### 예제 (브라우저는 인식되는 첫 번째 이미지 형식을 사용합니다.)

```html
<picture>
  <source srcset="img_avatar.png">
  <source srcset="img_girl.jpg">
  <img src="img_beatles.gif" alt="Beatles" style="width:auto;">
</picture>
```
  
{: .box-note}
**Note:** 브라우저는 일치하는 속성 값을 가진 첫 번째 ```<source>``` 요소를 사용하며 다음 ```<source>``` 요소는 무시합니다.
