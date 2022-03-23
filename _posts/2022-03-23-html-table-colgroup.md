---
layout: post
title: HTML 15-7. 테이블 열 그룹 (Table Colgroup)
subtitle: colgroup 요소는 테이블의 특정 열을 스타일링하기 위해 사용됩니다
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 테이블 열 그룹

## HTML 테이블 열 그룹

테이블의 첫 번째 두 열을 스타일링하려면 ```<colgroup>``` 및 ```<col>``` 요소를 사용합니다.

![html_table_colgroup_01](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table_colgroup_01.PNG?raw=true)

```<colgroup>``` 요소는 컬럼 사양의 컨테이너로 사용해야 합니다.

각 그룹은 ```<col>``` 요소로 지정됩니다.

```span``` 속성은 스타일을 가져올 열 수를 지정합니다.

```style``` 속성은 열에 부여할 스타일을 지정합니다.

###### 예제 1

```html
<table>
  <colgroup>
    <col span="2" style="background-color: #D6EEEE">
  </colgroup>
  <tr>
    <th>MON</th>
    <th>TUE</th>
    <th>WED</th>
    <th>THU</th>
...
```

{: .box-note}
**Note:** ```<colgroup>``` 태그는 ```<table>``` 요소의 자식이어야 하며 ```<thead>```, ```<tr>```, ```<td>``` 등의 다른 테이블 요소 앞에 배치해야 합니다. 단, ```<caption>``` 요소 뒤에 배치해야 합니다.

## 다중 열 요소

다른 스타일로 더 많은 컬럼을 스타일링하려면 ```<colgroup>``` 내에서 더 많은 ```<col>``` 요소를 사용합니다.

###### 예제 2

```html
<table>
  <colgroup>
    <col span="2" style="background-color: #D6EEEE">
    <col span="3" style="background-color: pink">
  </colgroup>
  <tr>
    <th>MON</th>
    <th>TUE</th>
    <th>WED</th>
    <th>THU</th>
...
```

## 빈 Colgroup


테이블 중앙에 열을 스타일링하려면 앞에 있는 열에 대해 "빈" ```<col>``` 요소(스타일 없음)를 삽입합니다.

###### 예제 3

```html
<table>
  <colgroup>
    <col span="3">
    <col span="2" style="background-color: pink">
  </colgroup>
  <tr>
    <th>MON</th>
    <th>TUE</th>
    <th>WED</th>
    <th>THU</th>
...
```

## 열 숨기기

```visibility: collapse``` 속성으로 열을 숨길 수 있습니다.

###### 예제 4

```html
<table>
  <colgroup>
    <col span="2">
    <col span="3" style="visibility: collapse">
  </colgroup>
  <tr>
    <th>MON</th>
    <th>TUE</th>
    <th>WED</th>
    <th>THU</th>
...
```
