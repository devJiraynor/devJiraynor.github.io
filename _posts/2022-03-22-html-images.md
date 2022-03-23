---
layout: post
title: HTML 13. 이미지 (Images)
subtitle: 이미지는 웹 페이지의 디자인과 모양을 개선할 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 이미지

## HTML 이미지 구문

HTML ```<img>``` 태그는 이미지를 웹 페이지에 삽입하기 위해 사용됩니다.

이미지는 기술적으로 웹 페이지에 삽입되는 것이 아니라 웹 페이지에 링크됩니다. ```<img>``` 태그는 참조된 이미지의 보관 공간을 만듭니다.

```<img>``` 태그는 비어 있으며 속성만 포함되어 있으며 닫힘 태그는 없습니다.

```<img>``` 태그에는 다음 두 가지 필수 속성이 있습니다.

+ ```src``` - 이미지의 경로를 지정합니다.
+ ```alt``` - 이미지에 대한 대체 텍스트를 지정합니다.

```html
<img src="경로" alt="대체 텍스트">
```

## src 속성

```src``` 속성은 필수이며 이미지에 대한 경로(URL)를 지정합니다.

{: .box-note}
**Note:** 웹 페이지가 로드될 때 웹 서버에서 이미지를 가져와 페이지에 삽입하는 것은 브라우저입니다. 따라서 웹 페이지와 관련하여 이미지가 실제로 동일한 위치에 있는지 확인하십시오. 그렇지 않으면 방문자에게 끊어진 링크 아이콘이 나타납니다. 브라우저가 이미지를 찾을 수 없는 경우 끊어진 링크 아이콘과 ```alt``` 텍스트가 표시됩니다.

###### 예제 1

```html
<img src="img_chania.jpg" alt="Flowers in Chania">
```

## alt 속성

```alt``` 속성은 필수이며 어떤 이유로 사용자가 이미지를 볼 수 없는 경우(연결 속도가 느리거나 ```src``` 속성의 오류가 발생하거나 사용자가 화면 리더를 사용하는 경우) 이미지에 대한 대체 텍스트를 제공합니다.

```alt``` 속성 값은 이미지 설명을 기술해야 합니다.

###### 예제 2

```html
<img src="img_chania.jpg" alt="Flowers in Chania">
```

브라우저가 이미지를 찾을 수 없는 경우 ```alt``` 속성 값이 표시됩니다.

```html
<img src="wrongname.gif" alt="Flowers in Chania">
```

{: .box-note}
**Tip:** 스크린 리더는 HTML 코드를 읽고 사용자가 콘텐츠를 "듣기" 할 수 있도록 하는 소프트웨어 프로그램입니다. 화면 리더는 시각장애인이거나 학습장애인에게 유용합니다.

## 이미지 크기 - Width 와 Height

```style``` 속성을 사용하여 이미지의 너비와 높이를 지정할 수 있습니다.

###### 예제 3

```html
<img src="img_girl.jpg" alt="Girl in a jacket" style="width:500px;height:600px;">
```

또는 다음과 같은 ```width``` (너비) 와 ```heigt``` (높이) 속성을 사용할 수 있습니다.

```html
<img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600">
```

```width``` 및 ```height``` 속성은 항상 이미지의 너비와 높이를 픽셀 단위로 정의합니다.

{: .box-note}
**Note:** 항상 이미지의 ```width```와 ```height``` 를 지정하십시오. 너비와 높이를 지정하지 않으면 이미지가 로드되는 동안 웹 페이지가 깜박일 수 있습니다.

## Width 와 Height? 아니면 Style?

```width``` , ```height``` 및 ```style``` 속성은 모두 HTML에서 유효합니다.

그러나 ```style``` 속성을 사용하는 것이 좋습니다. 스타일 시트가 이미지의 크기를 변경하는 것을 방지합니다.

###### 예제 4

```html
<!DOCTYPE html>
<html>
<head>
<style>
img {
  width: 100%;
}
</style>
</head>
<body>

<img src="html5.gif" alt="HTML5 Icon" width="128" height="128">

<img src="html5.gif" alt="HTML5 Icon" style="width:128px;height:128px;">

</body>
</html>
```

## 다른 폴더의 이미지

이미지가 하위 폴더에 있는 경우 ```src``` 속성에 폴더 이름을 포함해야 합니다.

###### 예제 5

```html
<img src="/images/html5.gif" alt="HTML5 Icon" style="width:128px;height:128px;">
```

## 다른 서버/웹 사이트의 이미지

일부 웹 사이트는 다른 서버의 이미지를 가리킵니다.

다른 서버상의 이미지를 포인트 하려면 , ```src``` 어트리뷰트에 절대(풀) URL 를 지정할 필요가 있습니다.

###### 예제 6

```html
<img src="https://www.w3schools.com/images/w3schools_green.jpg" alt="W3Schools.com">
```

**외부 이미지에 대한 주의사항** : 외부 이미지는 저작권에 속할 수 있습니다. 사용허가를 받지 못할 경우 저작권법 위반이 될 수 있습니다. 또한 외부 이미지는 제어할 수 없습니다. 갑자기 제거되거나 변경될 수 있습니다.

## 애니메이션 이미지

HTML에서는 애니메이션 GIF를 사용할 수 있습니다.

###### 예제 7

```html
<img src="programming.gif" alt="Computer Man" style="width:48px;height:48px;">
```

## 링크로서의 이미지

이미지를 링크로 사용하려면 ```<a>``` 태그 안에 ```<img>``` 태그를 넣습니다.

###### 예제 8

```html
<a href="default.asp">
  <img src="smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;">
</a>
```

## 이미지 플로팅

CSS ```float``` 속성을 사용하여 이미지를 텍스트의 오른쪽 또는 왼쪽으로 이동합니다.

###### 예제 9

```html
<p><img src="smiley.gif" alt="Smiley face" style="float:right;width:42px;height:42px;">
이미지가 텍스트 오른쪽으로 이동합니다.</p>

<p><img src="smiley.gif" alt="Smiley face" style="float:left;width:42px;height:42px;">
이미지가 텍스트 왼쪽으로 이동합니다.</p>
```

## 일반적인 이미지 형식

다음은 모든 브라우저(Chrome, Edge, Firefox, Safari, Opera)에서 지원되는 가장 일반적인 이미지 파일 형식입니다.

| 이름 | 파일 형식 | 확장자 |
| APNG | 휴대용 네트워크 애니메이션 그래픽스 (Animated Portable Network Graphics) | .apng |
|GIF| 그래픽스 교환 포맷 (Graphics Interchange Format) | .gif |
|ICO| Microsoft 아이콘 (Microsoft Icon) | .ico, .cur |
|JPEG| 공동 사진 전문가 그룹 이미지 (Joint Photographic Expert Group image) | .jpg, .jpeg, .jfif, .pjpeg, .pjp |
|PNG| 휴대용 네트워크 그래픽스 (Portable Network Graphics) | .png |
|SVG| 스케일러블 벡터 그래픽스 (Scalable Vector Graphics) | .svg |

## Summary

+ HTML ```<img>``` 요소를 사용하여 이미지를 정의합니다.
+ HTML ```src``` 속성을 사용하여 이미지의 URL을 정의합니다.
+ 표시할 수 없는 이미지의 대체 텍스트를 정의하려면 HTML ```alt``` 속성을 사용합니다.
+ HTML 폭 및 높이 속성 또는 CSS ```width``` 및 ```heigt``` 속성을 사용하여 이미지 크기를 정의합니다.
+ 이미지를 왼쪽 또는 오른쪽으로 띄우려면 CSS ```float``` 속성을 사용합니다.

{: .box-note}
**Note:** 큰 이미지를 로드하는 데 시간이 걸리고 웹 페이지가 느려질 수 있습니다. 이미지를 신중하게 사용하십시오.
