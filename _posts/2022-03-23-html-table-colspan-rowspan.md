---
layout: post
title: HTML 15-5. 테이블 colspan 및 rowspan (Tables Colspan & Rowspan)
subtitle: HTML 테이블에는 여러 행 및/또는 열에 걸쳐 셀이 포함될 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 테이블 colspan 및 rowspan

## HTML 테이블 - Colspan

셀 범위를 여러 열에 걸쳐서 설정하려면 ```colspan``` 속성을 사용합니다.

###### 예제 1

```html
<table>
  <tr>
    <th colspan="2">Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>43</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>57</td>
  </tr>
</table>
```

{: .box-note}
**Note:** ```colspan``` 속성 값은 걸칠 열의 수를 나타냅니다.

## HTML 테이블 - Rowspan

셀 범위를 여러 행에 걸쳐 설정하려면 ```rowspan``` 속성을 사용합니다.

###### 예제 2

```html
<table>
  <tr>
    <th>Name</th>
    <td>Jill</td>
  </tr>
  <tr>
    <th rowspan="2">Phone</th>
    <td>555-1234</td>
  </tr>
  <tr>
    <td>555-8745</td>
</tr>
</table>
```

{: .box-note}
**Note:** ```rowspan``` 속성 값은 걸칠 행의 수를 나타냅니다.
