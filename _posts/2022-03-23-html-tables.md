---
layout: post
title: HTML 15. 테이블 (Tables)
subtitle: HTML 테이블은 웹 개발자가 데이터를 행과 열에 정렬할 수 있도록 합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 테이블

## HTML 테이블 정의

HTML의 테이블은 행과 열 내부의 테이블 셀로 구성됩니다.

###### 예제 1

```html
<table>
  <tr>
    <th>Company</th>
    <th>Contact</th>
    <th>Country</th>
  </tr>
  <tr>
    <td>Alfreds Futterkiste</td>
    <td>Maria Anders</td>
    <td>Germany</td>
  </tr>
  <tr>
    <td>Centro comercial Moctezuma</td>
    <td>Francisco Chang</td>
    <td>Mexico</td>
  </tr>
</table>
```

## 테이블 셀

각 테이블 셀은 ```<td>``` 태그와 ```</td>``` 태그로 정의됩니다.

{: .box-note}
```td``` stands for table data.
