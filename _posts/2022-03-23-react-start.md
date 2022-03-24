---
layout: post
title: React 02. 시작하기
subtitle: 프로덕션에서 React를 사용하려면 Node.js에 포함된 npm이 필요합니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React 시작하기

{: .box-note}
프로덕션에서 React를 사용하려면 Node.js에 포함된 npm이 필요합니다.

React에 대한 개요를 보려면 HTML로 React 코드를 직접 작성할 수 있습니다.

그러나 React를 운영 환경에서 사용하려면 npm과 Node.js가 설치되어 있어야 합니다.

## HTML에서 React 직접 사용하기

React를 배우기 시작하는 가장 빠른 방법은 HTML 파일에 React를 직접 쓰는 것입니다.

먼저 세 개의 스크립트를 포함합니다. 처음 두 개는 JavaScripts에 React 코드를 쓰고 세 번째인 Babel은 오래된 브라우저에 JSX 구문과 ES6를 쓸 수 있습니다.

###### 예제 1 - HTML 파일에 3개의 CDN include

```html
<!DOCTYPE html>
<html>
  <head>
    <script src="https://unpkg.com/react@17/umd/react.development.js" crossorigin></script>
    <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js" crossorigin></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
  </head>
  <body>

    <div id="mydiv"></div>

    <script type="text/babel">
      function Hello() {
        return <h1>Hello World!</h1>;
      }

      ReactDOM.render(<Hello />, document.getElementById('mydiv'))
    </script>

  </body>
</html>
```

이 방법으로 React를 사용하는 것은 테스트 목적에는 문제가 없지만 **실제 환경**에서는 React 환경을 설정해야 합니다.

## React 개발환경 구축

npx 및 Node.js가 설치되어 있는 경우 ```create-react-app``` 을 사용하여 React 애플리케이션을 생성할 수 있습니다.

{: .box-note}
이전에 ```create-react-app``` 을 글로벌로 설치한 경우 패키지를 제거하여 npx가 항상 최신 버전의 ```create-react-app``` 을 사용하도록 하는 것이 좋습니다. 제거하려면 ```npm uninstall -g create-react-app``` 명령을 실행합니다.

다음 명령을 실행하여 ```my-react-app``` 이라는 이름의 React 응용 프로그램을 만듭니다.

```
npx create-react-app my-react-app
```

```create-react-app``` 은 React 응용 프로그램을 실행하는 데 필요한 모든 것을 설정합니다.

## React 응용 프로그램 실행

이제 첫 번째 React 응용 프로그램을 실행할 준비가 되었습니다.

다음 명령을 실행하여 ```my-react-app``` 디렉토리로 이동합니다.

```
cd my-react-app
```

다음 명령을 실행하여 React 응용 프로그램 ```my-react-app``` 을 실행합니다.

```
npm start
```

새로 만든 리액트 앱과 함께 새 브라우저 창이 나타납니다! 그렇지 않으면 브라우저를 열고 주소 표시줄에 ```localhost:3000``` 을 입력합니다.

## React 응용 프로그램 수정

```my-react-app``` 디렉토리를 보면 ```src``` 폴더가 있습니다. ```src``` 폴더 안에는 ```App.js``` 라는 파일이 있습니다.이 파일을 열면 다음과 같습니다.

###### /myReactApp/src/App.js:

```javascript
import logo from './logo.svg';
import './App.css';

function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Edit <code>src/App.js</code> and save to reload.
        </p>
        <a
          className="App-link"
          href="https://reactjs.org"
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
    </div>
  );
}

export default App;
```

HTML 내용을 변경하고 파일을 저장해 보십시오.

{: .box-note}
변경 내용은 파일을 저장한 직후에 표시되므로 브라우저를 새로고침할 필요가 없습니다.

###### 예제 2

```<div className="App">``` 내의 모든 콘텐츠를 ```<h1>``` 요소로 바꿉니다.

```javascript
function App() {
  return (
    <div className="App">
      <h1>Hello World!</h1>
    </div>
  );
}

export default App;
```

{: .box-note}
불필요한 Import(logo.svg 및 App.css)는 삭제되어 있습니다.

## 다음에 할 일은?

이제 컴퓨터에 React Environment가 설치되어 React에 대해 자세히 알아볼 준비가 되었습니다.

이 튜토리얼의 나머지 부분에서는 "Show React" 도구를 사용하여 React의 다양한 측면과 브라우저에 표시되는 방법을 설명합니다.

컴퓨터에서 동일한 단계를 수행하려면 먼저 ```src``` 폴더를 제거하여 ```index.js``` 파일을 하나만 포함합니다. 또한 ```index.js``` 파일 내의 불필요한 코드 행을 삭제하여 아래의 "Show React" 도구의 예시와 동일하게 만들어야 합니다.

###### 예제 3

```index.js``` : 

```javascript
import React from 'react';
import ReactDOM from 'react-dom';

const myfirstelement = <h1>Hello React!</h1>

ReactDOM.render(myfirstelement, document.getElementById('root'));
```

