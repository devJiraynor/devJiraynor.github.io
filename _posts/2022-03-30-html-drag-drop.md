---
layout: post
title: HTML 48. 드래그 앤 드롭 API (Drag and Drop API)
subtitle: HTML 에서는 임의의 요소를 드래그 해 드롭 할 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 드래그 앤 드롭 API

## 드래그 앤 드롭

드래그 앤 드롭은 매우 일반적인 기능입니다. 오브젝트를 "그랩"하여 다른 위치로 드래그하는 경우입니다.

## 지원 브라우저

| 브라우저 | 구글 Chrome | 마이크로소프트 Edge | Firefox | Safari | Opera |
| 버전 | 4.0 | 9.0 | 3.5 | 6.0 | 12.0 |

## HTML 드래그 앤 드롭 예제

다음은 드래그 앤 드롭의 간단한 예입니다.

```html
<!DOCTYPE HTML>
<html>
<head>
<script>
function allowDrop(ev) {
  ev.preventDefault();
}

function drag(ev) {
  ev.dataTransfer.setData("text", ev.target.id);
}

function drop(ev) {
  ev.preventDefault();
  var data = ev.dataTransfer.getData("text");
  ev.target.appendChild(document.getElementById(data));
}
</script>
</head>
<body>

<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"></div>

<img id="drag1" src="img_logo.gif" draggable="true" ondragstart="drag(event)" width="336" height="69">

</body>
</html>
```

복잡해 보일 수도 있지만 드래그 앤 드롭 이벤트의 다양한 부분을 살펴보도록 하겠습니다.

## 드래그 가능한 요소 만들기

먼저 요소를 끌 수 있도록 설정하려면 ```draggable``` 속성을 ```true```로 설정합니다.

```html
<img draggable="true">
```

## 드래그 대상 - ```ondragstart``` 및 ```setData()```

그런 다음 요소를 끌었을 때 수행할 작업을 지정합니다.

위의 예에서는 ```ondragstart``` 속성이 드래그할 데이터를 지정하는 함수 drag(이벤트)를 호출합니다.

```dataTransfer.setData()``` 메서드는 드래그된 데이터의 데이터 유형과 값을 설정합니다.

```javascript
function drag(ev) {
  ev.dataTransfer.setData("text", ev.target.id);
}
```

이 경우 데이터 유형은 "text"이고 값은 드래그 요소의 ID("drag1") 입니다.

## 드롭 위치 - 드래그오버 ```ondragover```

이벤트 ```ondragover``` 는 드래그된 데이터를 드롭할 수 있는 위치를 지정합니다.

기본적으로는 데이터/요소는 다른 요소에서 삭제할 수 없습니다. 드롭을 허용하려면 요소의 기본 처리를 방지해야 합니다.

이를 수행하려면 ```ondragover``` 이벤트에 대해 ```event.proventDefault()``` 메서드를 호출합니다.

```javascript
event.preventDefault()
```

## 드롭 - 드롭 실행

드래그된 데이터가 삭제되면 삭제 이벤트가 발생합니다.

위의 예에서는 ```ondrop``` 속성 함수 ```drop```(이벤트)을 호출합니다.

```javascript
function drop(ev) {
  ev.preventDefault();
  var data = ev.dataTransfer.getData("text");
  ev.target.appendChild(document.getElementById(data));
}
```

코드 설명:

+ 브라우저의 기본 데이터 처리를 방지하려면 ```prevent Default()```를 호출합니다.
+ ```dataTransfer.getData()``` 메서드를 사용하여 드래그된 데이터를 가져옵니다. 이 메서드는 ```setData()``` 메서드에서 동일한 유형으로 설정된 모든 데이터를 반환합니다.
+ 드래그된 데이터는 드래그된 요소의 ID("drag1")입니다.
+ 드래그된 요소를 드롭 요소에 추가합니다.
