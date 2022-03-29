---
layout: post
title: React 25. React 커스텀 후크 (Custom Hook)
subtitle: 여러 컴포넌트에서 사용해야 하는 컴포넌트 로직이 있는 경우 해당 로직을 커스텀 후크로 추출할 수 있습니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React 커스텀 후크

후크는 재사용 가능한 함수입니다.

여러 컴포넌트에서 사용해야 하는 컴포넌트 로직이 있는 경우 해당 로직을 커스텀 후크로 추출할 수 있습니다.

커스텀 후크는 "use"로 시작합니다. 예: ```useFetch```.

## 후크 빌드

다음 코드에서는 Home 컴포넌트에서 데이터를 가져와 표시하고 있습니다.

JSONPlaceholder 서비스를 사용하여 가짜 데이터를 가져옵니다. 이 서비스는 기존 데이터가 없을 때 애플리케이션을 테스트하는 데 매우 적합합니다.

JSONPlaceholder 서비스를 사용하여 가짜 "todo" 항목을 가져와 페이지에 제목을 표시합니다.

###### 예제 1 - index.js

```javascript
import { useState, useEffect } from "react";
import ReactDOM from "react-dom";

const Home = () => {
  const [data, setData] = useState(null);

  useEffect(() => {
    fetch("https://jsonplaceholder.typicode.com/todos")
      .then((res) => res.json())
      .then((data) => setData(data));
 }, []);

  return (
    <>
      {data &&
        data.map((item) => {
          return <p key={item.id}>{item.title}</p>;
        })}
    </>
  );
};

ReactDOM.render(<Home />, document.getElementById("root"));
```

```fetch``` 로직은 다른 컴포넌트에서도 필요할 수 있으므로 custom hook으로 추출합니다.

custom hook으로 사용할 파일로 ```fetch``` 로직을 이동합니다.

###### 예제 2 - useFetch.js

```javascript
import { useState, useEffect } from "react";

const useFetch = (url) => {
  const [data, setData] = useState(null);

  useEffect(() => {
    fetch(url)
      .then((res) => res.json())
      .then((data) => setData(data));
  }, [url]);

  return [data];
};

export default useFetch;
```

###### 예제 2 - index.js

```javascript
import ReactDOM from "react-dom";
import useFetch from "./useFetch";

const Home = () => {
  const [data] = useFetch("https://jsonplaceholder.typicode.com/todos");

  return (
    <>
      {data &&
        data.map((item) => {
          return <p key={item.id}>{item.title}</p>;
        })}
    </>
  );
};

ReactDOM.render(<Home />, document.getElementById("root"));
```

## 예제 설명

```useFetch```를 포함하고 있는 ```useFetch.js```라는 새로운 파일을 만들었습니다. 이 파일에는 데이터를 ```fetch```에 필요한 모든 로직이 포함되어 있습니다.

하드 코드화된 url을 삭제하고 커스텀 후크에 전달할 수 있는 ```url``` 변수로 대체했습니다.

마지막으로 Hook에서 데이터를 반환하겠습니다.

```index.js```에서는 ```useFetch``` Hook을 import하여 다른 Hook과 동일하게 활용하고 있습니다. 여기서 데이터를 가져올 URL을 전달합니다.

이제 이 커스텀 후크를 임의의 컴포넌트에서 재사용하여 임의의 URL에서 데이터를 가져올 수 있습니다.
