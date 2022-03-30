---
layout: post
title: HTML 15-1. 테이블 테두리 (Table Borders)
subtitle: HTML 테이블은 다양한 스타일과 모양의 테두리를 가질 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 테이블 테두리

## 테두리 추가 방법

표에 테두리를 추가할 때 각 표 셀 주위에 테두리도 추가합니다.

![html_table_borders_01](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table_borders_01.PNG?raw=true)

테두리를 추가하려면 ```table```, ```th``` 및 ```td``` 요소에 CSS ```border``` 속성을 사용합니다.

###### 예제 1

```css
table, th, td {
  border: 1px solid black;
}
```

## Collapsed 테이블 테두리

위의 예시와 같이 이중 테두리가 생기지 않도록 CSS ```border-collapse``` 속성을 ```collapse```로 설정합니다.

이렇게 하면 테두리가 단일 테두리로 축소됩니다.

![html_table_borders_02](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table_borders_02.PNG?raw=true)

###### 예제 2

```css
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}
```

## 테이블 테두리 스타일

각 셀의 배경색을 설정하고 테두리를 흰색(문서 배경과 동일)으로 지정하면 보이지 않는 테두리처럼 보입니다.

![html_table_borders_03](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table_borders_03.PNG?raw=true)

###### 예제 3

```css
table, th, td {
  border: 1px solid white;
  border-collapse: collapse;
}
th, td {
  background-color: #96D4D4;
}
```

## 테이블 테두리 라운드

```border-radius``` 속성을 사용하면 테두리가 둥근 모서리가 됩니다.

![html_table_borders_04](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table_borders_04.PNG?raw=true)

###### 예제 4

```html
table, th, td {
  border: 1px solid black;
  border-radius: 10px;
}
```

css 셀렉터에서 테이블을 생략하면 테이블 주위의 경계를 건너뜁니다.

![html_table_borders_05](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table_borders_05.PNG?raw=true)

###### 예제 5

```css
th, td {
  border: 1px solid black;
  border-radius: 10px;
}
```

## 도트 테이블 테두리

```border-style``` 특성을 사용하여 테두리 속성을 설정할 수 있습니다.

![html_table_borders_06](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table_borders_06.PNG?raw=true)

다음 값이 사용됩니다.

![html_table_borders_07](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table_borders_07.PNG?raw=true)

###### 예제 6

```css
th, td {
  border-style: dotted;
}
```

## 테두리 색상

```border-color``` 속성을 사용하여 테두리 색상을 설정할 수 있습니다.

![html_table_borders_08](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table_borders_08.PNG?raw=true)

###### 예제 7

```css
th, td {
  border-color: #96D4D4;
}
```
