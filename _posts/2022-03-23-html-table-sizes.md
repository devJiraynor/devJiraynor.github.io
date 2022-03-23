---
layout: post
title: HTML 15-2. 테이블 사이즈 (Table size)
subtitle: HTML 테이블은 열, 행 또는 테이블 전체에 따라 크기가 다를 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 테이블 사이즈

```width``` 또는 ```height``` 특성과 함께 ```style``` 속성을 사용하여 테이블, 행 또는 열의 크기를 지정합니다.

## HTML 테이블 너비

테이블의 너비를 설정하려면 ```style``` 속성을 ```<table>``` 요소에 추가합니다.

###### 예제 (테이블의 폭을 100%로 설정합니다.)

```html
<table style="width:100%">
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

{: .box-note}
**Note:** 폭의 크기 단위로 퍼센티지를 사용하면 이 요소가 부모 요소(이 경우 ```<body>``` 요소)와 비교되는 폭이 됩니다.

## HTML 테이블 열 너비

![html_table_size_01](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table_size_01.PNG?raw=true)

특정 컬럼 크기를 설정하려면 ```<th>``` 또는 ```<td>``` 요소에 ```style``` 속성을 추가합니다.

###### 예제 (첫 번째 열의 너비를 70%로 설정합니다.)

```html
<table style="width:100%">
  <tr>
    <th style="width:70%">Firstname</th>
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

## HTML 테이블 행 높이

![html_table_size_02](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table_size_02.PNG?raw=true)

특정 행의 높이를 설정하려면 테이블 행 요소에 ```style``` 속성을 추가합니다.

###### 예제 (두 번째 줄의 높이를 200픽셀로 설정합니다.)

```html
<table style="width:100%">
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
    <th>Age</th>
  </tr>
  <tr style="height:200px">
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

