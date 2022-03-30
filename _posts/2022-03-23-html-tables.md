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
```td```는 테이블 데이터를 나타냅니다.

```<td>``` 와 ```</td>``` 사이의 모든 내용은 테이블 셀의 내용입니다.

###### 예제 2

```html
<table>
  <tr>
    <td>Emil</td>
    <td>Tobias</td>
    <td>Linus</td>
  </tr>
</table>
```

{: .box-note}
**Note:** 테이블 데이터 요소는 테이블의 데이터 컨테이너입니다. 텍스트, 이미지, 목록, 기타 테이블 등 모든 종류의 HTML 요소를 포함할 수 있습니다.

## 테이블 행

각 테이블 행은 ```<tr>``` 로 시작하여 ```</tr>``` 태그로 끝납니다.

{: .box-note}
```tr``` 은 테이블 행을 나타냅니다.

###### 예제 3

```html
<table>
  <tr>
    <td>Emil</td>
    <td>Tobias</td>
    <td>Linus</td>
  </tr>
  <tr>
    <td>16</td>
    <td>14</td>
    <td>10</td>
  </tr>
</table>
```

표에 원하는 수의 행을 포함할 수 있습니다. 각 행의 셀 수가 동일한지 확인하십시오.

{: .box-note}
**Note:** 행에 셀이 다른 행보다 적거나 많을 수 있습니다. 그것에 대해서는 다음 장에서 배울 것이다.

## 테이블 머리글

셀을 헤더로 할 수 있습니다. 이 경우 ```<td>``` 태그 대신 ```<th>``` 태그를 사용합니다.

###### 예제 4

```html
<table>
  <tr>
    <th>Person 1</th>
    <th>Person 2</th>
    <th>Person 3</th>
  </tr>
  <tr>
    <td>Emil</td>
    <td>Tobias</td>
    <td>Linus</td>
  </tr>
  <tr>
    <td>16</td>
    <td>14</td>
    <td>10</td>
  </tr>
</table>
```

디폴트로는 ```<th>``` 요소의 텍스트는 굵은 글씨로 가운데에 표시됩니다만, CSS 를 사용해 변경할 수 있습니다.
