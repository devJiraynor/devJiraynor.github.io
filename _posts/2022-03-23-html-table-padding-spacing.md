---
layout: post
title: HTML 15-4. 테이블 패딩 및 스페이싱 (Tables)
subtitle: HTML 테이블은 셀 내부의 패딩과 셀 사이의 공간을 조정할 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 테이블 패딩 및 스페이싱

## HTML 테이블 셀 패딩

셀 패딩은 셀 가장자리와 셀 내용 사이의 공간입니다.

디폴트로 패딩은 0 으로 설정되어 있습니다.

테이블 셀에 패딩을 추가하려면 CSS ```padding``` 속성을 사용합니다.

###### 예제 1

```html
th, td {
  padding: 15px;
}
```

내용 위에만 패딩을 추가하려면 ```padding-top``` 속성을 사용합니다.

다른 쪽에는 ```padding-bottom```, ```padding-left``` 및 ```padding-right``` 속성이 있습니다.

###### 예제 2

```html
th, td {
  padding-top: 10px;
  padding-bottom: 20px;
  padding-left: 30px;
  padding-right: 40px;
}
```

## HTML 테이블 셀 스페이싱

셀 간격은 각 셀 사이의 간격입니다.

기본적으로 공간은 2픽셀로 설정되어 있습니다.

테이블 셀 사이의 공간을 변경하려면 ```table``` 요소의 CSS ```border-spacing``` 을 사용합니다.

###### 예제 3

```html
table {
  border-spacing: 30px;
}
```
