---
layout: post
title: HTML 15-6. 테이블 스타일링 (Table Styling)
subtitle: CSS를 사용하여 테이블을 보다 보기 좋게 만듭니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 테이블 스타일링

## HTML 테이블 - 얼룩말 스트라이프

테이블 열마다 배경색을 추가하면 멋진 얼룩말 스트라이프 효과를 낼수 있니다.

![html_table-styling_01](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table-styling_01.PNG?raw=true)

다른 모든 테이블 행 요소를 스타일링하려면 ```:nth-child(even)``` 셀렉터를 다음과 같이 사용합니다.

###### 예제 1

```html
tr:nth-child(even) {
  background-color: #D6EEEE;
}
```

{: .box-note}
**Note:** ```(even)``` 대신 ```(odd)``` 를 사용하면 2,4,6 등이 아닌 1,3,5 행 등에서 스타일링이 이루어집니다.

## HTML 테이블 - 수직 얼룩말 스트라이프

수직 얼룩말 줄무늬를 만들려면 한 줄씩이 아니라 한 줄 간격으로 스타일을 지정합니다.

![html_table-styling_02](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table-styling_02.PNG?raw=true)

다음과 같이 테이블 데이터 요소의 ```:nth-child(even)``` 를 설정합니다.

###### 예제 2

```html
td:nth-child(even), th:nth-child(even) {
  background-color: #D6EEEE;
}
```

{: .box-note}
**Note:** 헤더와 일반 테이블셀 모두 스타일링을 하려면 ```:nth-child()``` 셀렉터를 ```th``` 와 ```td``` 요소 모두에 배치합니다.

## 수직 줄무늬와 수평 줄무늬 조합

위의 두 가지 예에서 스타일을 조합할 수 있으며, 각 행과 다른 열에 스트라이프가 있습니다.

투명 컬러를 사용하면 겹치는 효과가 있습니다.

![html_table-styling_03](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table-styling_03.PNG?raw=true)

```rgba()``` 색상을 사용하여 색상의 투명도를 지정합니다.

###### 예제 3

```html
tr:nth-child(even) {
  background-color: rgba(150, 212, 212, 0.4);
}

th:nth-child(even),td:nth-child(even) {
  background-color: rgba(150, 212, 212, 0.4);
}
```

## 수평 칸막이

![html_table-styling_04](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table-styling_04.PNG?raw=true)

각 테이블 행의 맨 아래에만 경계를 지정하는 경우 수평 구분선이 있는 테이블이 표시됩니다.

모든 ```tr``` 요소에 ```border-bottom``` 특성을 추가하여 수평 구분선을 가져옵니다.

###### 예제 4

```html
tr {
  border-bottom: 1px solid #ddd;
}
```

## 호버블 테이블

```tr``` 의 ```:hover``` 셀렉터를 사용하여 마우스 위의 테이블 행을 강조 표시합니다.

![html_table-styling_05](https://github.com/devJiraynor/devJiraynor.github.io/blob/master/assets/img/html/html_table-styling_05.PNG?raw=true)

###### 예제 5

```html
tr:hover {background-color: #D6EEEE;}
```

