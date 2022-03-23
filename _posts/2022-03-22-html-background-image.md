---
layout: post
title: HTML 13-2. 배경 이미지 (Background Image)
subtitle: 거의 모든 HTML 요소에 대해 배경 이미지를 지정할 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 배경 이미지

## HTML 요소의 배경 이미지

HTML 요소에 배경 이미지를 추가하려면 HTML ```style``` 속성 및 CSS ```background-image``` 속성을 사용합니다.

###### 예제 (HTML 요소에 배경 이미지 추가)

```html
<p style="background-image: url('img_girl.jpg');">
```

```<style>``` 요소의 ```<head>``` 섹션에서 배경 이미지를 지정할 수도 있습니다.

###### 예제 (```<style>``` 요소로 배경 이미지를 지정합니다.)

```html
<style>
p {
  background-image: url('img_girl.jpg');
}
</style>
```

## 페이지의 배경 이미지

페이지 전체에 배경이미지를 삽입할 때는 ```<body>``` 요소에 배경 이미지를 지정합니다.

###### 예제 (전체 페이지의 배경 이미지 추가)

```html
<style>
body {
  background-image: url('img_girl.jpg');
}
</style>
```

## 배경이미지 반복

배경 이미지가 요소보다 작으면 이미지가 요소의 끝에 도달할 때까지 수평 및 수직으로 반복됩니다.

![html-background-image-01](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_background_image_01.PNG?raw=true)

###### 예제

```html
<style>
body {
  background-image: url('example_img_girl.jpg');
}
</style>
```

배경 이미지가 반복되지 않도록 하려면 ```background-repeat``` 속성을 ```no-repeat``` 으로 설정하십시오.

```html
<style>
body {
  background-image: url('example_img_girl.jpg');
  background-repeat: no-repeat;
}
</style>
```

## 배경 커버

배경 이미지가 ```cover``` 요소를 포함하도록 하려면 포함할 ```background-size``` 특성을 설정할 수 있습니다.

또한 요소 전체가 항상 커버되도록 하려면 ```background-attachment``` 속성을 ```fixed``` 로 설정합니다.

이렇게 하면 배경 이미지가 스트레칭 없이 전체 요소를 덮습니다. (이미지는 원래 비율을 유지합니다).

```html
<style>
body {
  background-image: url('img_girl.jpg');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
}
</style>
```

## 배경 늘리기

배경 이미지를 전체 요소에 맞게 확장하려면 ```background-size``` 속성을 ```100% 100%``` 로 설정할 수 있습니다.

![html-background-image-02](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_background_image_02.PNG?raw=true)

브라우저 창의 크기를 조정하면 이미지가 확장되지만 항상 요소 전체를 덮는다는 것을 알 수 있습니다.

```html
<style>
body {
  background-image: url('img_girl.jpg');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: 100% 100%;
}
</style>
```
