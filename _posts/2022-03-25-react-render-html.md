---
layout: post
title: React 04. HTML 렌더링 (Render HTML)
subtitle: React의 목표는 웹 페이지에서 HTML을 렌더링하는 것입니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React HTML 렌더링

React는 ```ReactDOM.render()``` 라는 함수를 사용하여 HTML을 웹 페이지에 렌더링합니다.

## Render 함수

```ReactDOM.render()``` 함수는 HTML 코드와 HTML 요소의 두 가지 인수를 사용합니다.

이 함수의 목적은 지정된 HTML 요소 내에 지정된 HTML 코드를 표시하는 것입니다.

하지만 어디에 렌더링 될까요?

React 프로젝트의 루트 디렉터리에 "public" 이라는 이름의 다른 폴더가 있습니다. 이 폴더에는 ```index.html``` 파일이 있습니다.

이 파일 본문에 1개의 ```<div>``` 가 표시됩니다. 여기서 React 응용 프로그램이 렌더링됩니다.

###### 요소 내부의 단락을 "root" ID로 표시합니다.

```html
ReactDOM.render(<p>Hello</p>, document.getElementById('root'));
```

###### 결과는 ```<div id="root">``` 요소에 표시됩니다.

```html
<body>
  <div id="root"></div>
</body>
```

{: .box-note}
요소 ID를 "root"라고 부를 필요는 없지만 이것이 표준 규칙입니다.

## HTML 코드

HTML 코드는 JavaScript 코드 내에 HTML 태그를 쓸 수 있는 JSX를 사용합니다.

구문이 생소하더라도 걱정하지 마십시오. JSX에 대한 자세한 내용은 다음 장에서 배웁니다.

###### HTML 코드를 포함하는 변수를 생성하여 "root" 노드에 표시합니다.

```html
const myelement = (
  <table>
    <tr>
      <th>Name</th>
    </tr>
    <tr>
      <td>John</td>
    </tr>
    <tr>
      <td>Elsa</td>
    </tr>
  </table>
);

ReactDOM.render(myelement, document.getElementById('root'));
```

## 루트 노드

루트 노드는 결과를 표시하는 HTML 요소입니다.

리액트가 관리하는 콘텐츠를 담는 컨테이너와 같다.

반드시 ```<div>``` 요소일 필요는 없으며 ```id='root'``` 를 가질 필요도 없습니다.

###### 루트 노드는 원하는 대로 호출할 수 있습니다.

```html
<body>

  <header id="sandy"></header>

</body>
```

###### ```<header id="sandy">``` 요소에 결과를 표시합니다.

```html
ReactDOM.render(<p>Hallo</p>, document.getElementById('sandy'));
```
