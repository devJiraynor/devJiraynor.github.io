---
layout: post
title: React 16. Sass 스타일링 (Sass Styling)
subtitle: Sass는 CSS 프리프로세서입니다. sass 파일은 서버에서 실행되어 브라우저로 CSS가 전송됩니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React Sass 스타일링

## Sass 란

Sass는 CSS 프리프로세서입니다. 

sass 파일은 서버에서 실행되어 브라우저로 CSS가 전송됩니다.

## Sass 사용법

프로젝트에서 ```create-react-app```을 사용하면 React 프로젝트에서 Sass를 쉽게 설치하고 사용할 수 있습니다.

터미널에서 다음 명령을 실행하여 Sass를 설치합니다.

```
npm i sass
```

이제 Sass 파일을 프로젝트에 사용할 준비가 되었습니다.

## Sass 파일 생성

CSS 파일 작성과 같은 방법으로 Sass 파일을 작성합니다만, Sass 파일의 확장자는 ```.scss``` 입니다.

Sass 파일에서는 변수 및 기타 Sass 함수를 사용할 수 있습니다.

###### my-sass.scss - 텍스트의 색상을 정의하는 변수를 만듭니다.

```scss
$myColor: red;

h1 {
  color: $myColor;
}
```

CSS 파일을 import 했을 때와 같은 방법으로 Sass 파일을 import 합니다.

###### index.js

```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import './my-sass.scss';

const Header = () => {
  return (
    <>
      <h1>Hello Style!</h1>
      <p>Add a little style!.</p>
    </>
  );
}

ReactDOM.render(<Header />, document.getElementById('root'));
```
