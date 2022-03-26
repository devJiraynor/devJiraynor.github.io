---
layout: post
title: React 13. 라우터 (Router)
subtitle: Create React App에는 페이지 라우팅이 포함되어 있지 않습니다. 리액트 라우터는 가장 일반적인 솔루션입니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React 라우터

## React 라우터 추가

응용 프로그램에 React 라우터를 추가하려면 응용 프로그램의 루트 디렉토리에서 터미널로 다음 작업을 수행합니다.

```
npm i -D react-router-dom
```

{: .box-note}
이 튜토리얼에서는 React Router v6를 사용합니다. v5에서 업그레이드하는 경우 @latest 플래그를 사용해야 합니다.

```
npm i -D react-router-dom@latest
```

## 폴더 구조

여러 페이지 경로를 가진 응용프로그램을 만들려면 먼저 파일 구조화부터 시작하십시오.

```src``` 폴더 내에 여러 파일이 있는 ```pages```라는 이름의 폴더를 만듭니다.

```src\pages\```:
+ ```Layout.js```
+ ```Home.js```
+ ```Blogs.js```
+ ```Contact.js```
+ ```NoPage.js```

각 파일에는 매우 기본적인 React 컴포넌트가 포함되어 있습니다.

## 기본 사용법

이제 ```index.js``` 파일에서 라우터를 사용합니다.

###### 예제 1 - 리액트 라우터를 사용하여 URL을 기반으로 페이지로 라우팅합니다.

```index.js```:

```javascript
import ReactDOM from "react-dom";
import { BrowserRouter, Routes, Route } from "react-router-dom";
import Layout from "./pages/Layout";
import Home from "./pages/Home";
import Blogs from "./pages/Blogs";
import Contact from "./pages/Contact";
import NoPage from "./pages/NoPage";

export default function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Layout />}>
          <Route index element={<Home />} />
          <Route path="blogs" element={<Blogs />} />
          <Route path="contact" element={<Contact />} />
          <Route path="*" element={<NoPage />} />
        </Route>
      </Routes>
    </BrowserRouter>
  );
}

ReactDOM.render(<App />, document.getElementById("root"));
```

#### 예제 설명

먼저 ```<BrowserRouter>```로 콘텐츠를 정리합니다.

다음으로 ```<Routes>```를 정의합니다. 애플리케이션에는 복수의 ```<Routes>```를 설정할 수 있습니다. 이 기본 예에서는 하나만 사용합니다.

```<Route>```는 중복 할 수 있습니다. 첫 번째 ```<Route>```는 ```/```의 경로를 가지며 ```Layout``` 컴포넌트를 렌더링합니다.

중복된 ```<Route>```는 부모 루트를 상속하여 추가합니다. 따라서 ```blogs``` 경로가 부모와 결합되어 ```/blogs```가 됩니다.

```Home``` 컴포넌트 루트에는 경로는 없지만 ```index``` 속성이 있습니다. 이 루트를 부모 루트의 디폴트루트(```/```)로서 지정합니다.

```path```를 ```*```로 설정하면 정의되지 않은 URL에 대한 캐치올 역할을 합니다. 이것은 404 에러 페이지에 매우 적합합니다.

## 페이지와 컴포넌트

```Layout``` 컴포넌트에는 ```<Outlet>```과 ```<Link>``` 요소가 있습니다.

```<Outlet>```은 선택한 현재 루트를 렌더링합니다.

```<Link>```는 URL 설정 및 URL 이력 추적에 사용됩니다.

내부 경로에 링크할 때마다 ```<a href="">``` 대신 ```<Link>```를 사용합니다.

"layout route"는 탐색 메뉴와 같은 모든 페이지에 공통 컨텐츠를 삽입하는 공유 컴포넌트입니다.

###### Layout.js

```javascript
import { Outlet, Link } from "react-router-dom";

const Layout = () => {
  return (
    <>
      <nav>
        <ul>
          <li>
            <Link to="/">Home</Link>
          </li>
          <li>
            <Link to="/blogs">Blogs</Link>
          </li>
          <li>
            <Link to="/contact">Contact</Link>
          </li>
        </ul>
      </nav>

      <Outlet />
    </>
  )
};

export default Layout;
```

###### Home.js

```javascript
const Home = () => {
  return <h1>Home</h1>;
};

export default Home;
```

###### Blogs.js

```javascript
const Blogs = () => {
  return <h1>Blog Articles</h1>;
};

export default Blogs;
```

###### Contact.js

```javascript
const Contact = () => {
  return <h1>Contact Me</h1>;
};

export default Contact;
```

###### NoPage.js

```javascript
const NoPage = () => {
  return <h1>404</h1>;
};

export default NoPage;
```
