---
layout: post
title: HTML 15-3. 테이블 헤더 (Table Headers)
subtitle: HTML 테이블에는 각 열 또는 행 또는 여러 열/행에 대한 헤더가 있을 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 테이블 헤더

## HTML 테이블 헤더

테이블 헤더는 ```th``` 요소로 정의되며 각 ```th``` 요소는 테이블셀을 나타냅니다.

###### 예제 1

```html
<table>
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
</table>
```

## 수직 테이블 헤더

첫 번째 열을 테이블 헤더로 사용하려면 각 행의 첫 번째 셀을 ```th``` 요소로 정의합니다.

###### 예제 2

```html
<table>
  <tr>
    <th>Firstname</th>
    <td>Jill</td>
    <td>Eve</td>
  </tr>
  <tr>
    <th>Lastname</th>
    <td>Smith</td>
    <td>Jackson</td>
  </tr>
  <tr>
    <th>Age</th>
    <td>94</td>
    <td>50</td>
  </tr>
</table>
```

## 테이블 헤더 정렬

기본적으로 테이블 헤더는 굵은 글씨로 가운데에 표시됩니다.

![html_table_headers_01](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table_headers_01.PNG?raw=true)

테이블 헤더를 왼쪽 정렬하려면 CSS ```text-align``` 속성을 사용합니다.

###### 예제 3

```css
th {
  text-align: left;
}
```

## 여러 열의 헤더

헤더는 두 개 이상의 열에 걸쳐 있을 수 있습니다.

![html_table_headers_02](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table_headers_02.PNG?raw=true)

이를 수행하려면 ```<th>``` 요소의 ```colspan``` 속성을 사용합니다.

###### 예제 4

```html
<table>
  <tr>
    <th colspan="2">Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
</table>
```

## 테이블 캡션

전체 테이블의 제목으로 사용할 캡션을 추가할 수 있습니다.

![html_table_headers_03](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table_headers_03.PNG?raw=true)

테이블에 캡션을 추가하려면 ```<caption>``` 태그를 사용합니다.

###### 예제 5

```html
<table style="width:100%">
  <caption>Monthly savings</caption>
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
  <tr>
    <td>February</td>
    <td>$50</td>
  </tr>
</table>
```

{: .box-note}
**Note :** ```<caption>``` 태그는 ```<table>``` 태그 바로 뒤에 삽입해야 합니다.
