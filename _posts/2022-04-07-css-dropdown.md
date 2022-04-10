---
layout: post
title: CSS 33. 드롭다운 (Dropdowns)
subtitle: CSS를 사용하여 호버링 가능한 드롭다운을 만듭니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 드롭다운

## 기본 드롭다운

사용자가 요소 위로 마우스를 이동할 때 나타나는 드롭다운 상자를 만듭니다.

###### 예제 1

```html
<style>
.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  padding: 12px 16px;
  z-index: 1;
}

.dropdown:hover .dropdown-content {
  display: block;
}
</style>

<div class="dropdown">
  <span>Mouse over me</span>
  <div class="dropdown-content">
    <p>Hello World!</p>
  </div>
</div>
```

#### 예제 설명

**HTML:** 

임의의 요소를 사용하여 드롭다운 콘텐츠를 엽니다(예: ```<span>``` 또는 ```<button>``` 요소).

컨테이너 요소(예: ```<div>```)를 사용하여 드롭다운 콘텐츠를 만들고 그 안에 원하는 내용을 추가합니다.

CSS를 사용하여 드롭다운 콘텐츠를 올바르게 배치하려면 요소 주위에 ```<div>``` 요소를 감습니다.

**CSS:**

```.dropdown``` 클래스는 ```position:relative;```를 사용하며, 이는 드롭다운 콘텐츠를 드롭다운 버튼 바로 아래에 배치하려는 경우( ```position:absolute``` 사용)에 필요합니다.

```.dropdown-content``` 클래스는 실제 드롭다운 콘텐츠를 보유합니다. 기본적으로 숨겨져 있으며 호버에 표시됩니다. ```min-width```는 160px로 설정됩니다. 이것을 자유롭게 변경해 주세요. 

**Tip:** 드롭다운 콘텐츠의 너비를 드롭다운 버튼만큼 넓히려면 ```width```를 100%로 설정합니다(작은 화면에서 스크롤을 사용하려면 ```overflow:auto```).

테두리를 사용하는 대신 CSS ```box-shadow``` 속성을 사용하여 드롭다운 메뉴를 "카드"처럼 만들었습니다.

```:hover``` 셀렉터는 사용자가 마우스를 드롭다운 버튼 위로 이동할 때 드롭다운 메뉴를 표시하는 데 사용됩니다.

## 드롭다운 메뉴

사용자가 목록에서 옵션을 선택할 수 있는 드롭다운 메뉴를 만듭니다.

이 예는 드롭다운 상자 안에 링크를 추가하고 스타일 드롭다운 단추에 맞게 스타일을 지정한다는 점을 제외하면 이전 예와 유사합니다.

###### 예제 2

```html
<style>
/* 드롭다운 버튼 스타일링 */
.dropbtn {
  background-color: #4CAF50;
  color: white;
  padding: 16px;
  font-size: 16px;
  border: none;
  cursor: pointer;
}

/* 컨테이너 <div> - 드롭다운 컨텐츠 position 지정 필요 */
.dropdown {
  position: relative;
  display: inline-block;
}

/* 드롭다운 컨텐츠(기본적으로 숨김) */
.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}

/* 드롭다운 내부 링크 */
.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

/* 호버에서 드롭다운 링크 색상 변경 */
.dropdown-content a:hover {background-color: #f1f1f1}

/* 호버에 드롭다운 메뉴 표시 */
.dropdown:hover .dropdown-content {
  display: block;
}

/* 드롭다운 내용이 표시될 때 드롭다운 버튼의 배경색 변경 */
.dropdown:hover .dropbtn {
  background-color: #3e8e41;
}
</style>

<div class="dropdown">
  <button class="dropbtn">Dropdown</button>
  <div class="dropdown-content">
    <a href="#">Link 1</a>
    <a href="#">Link 2</a>
    <a href="#">Link 3</a>
  </div>
</div>
```

## 오른쪽 정렬 드롭다운

드롭다운 메뉴를 왼쪽에서 오른쪽으로 대신 오른쪽에서 왼쪽으로 이동시키려면 ```right: 0;```을 추가해야합니다.

###### 예제 3

```css
.dropdown-content {
  right: 0;
}
```

