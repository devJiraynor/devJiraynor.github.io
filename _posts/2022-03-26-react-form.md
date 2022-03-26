---
layout: post
title: React 12. 폼 (Form)
subtitle: HTML과 마찬가지로 React는 양식을 사용하여 사용자가 웹 페이지와 상호 작용할 수 있도록 합니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React 폼

## React에 폼 추가

다른 요소와 마찬가지로 React를 사용하여 폼을 추가합니다.

###### 예제 1 - 사용자가 이름을 입력할 수 있는 양식을 추가합니다.

```javascript
function MyForm() {
  return (
    <form>
      <label>Enter your name:
        <input type="text" />
      </label>
    </form>
  )
}
ReactDOM.render(<MyForm />, document.getElementById('root'));
```

정상적으로 동작하며 폼이 송신되어 페이지가 갱신됩니다.

그러나 이것은 리액트에서는 일반적인 방법이 아닙니다.

이 기본 동작을 방지하고 React가 폼을 제어할 수 있도록 합니다.

## 폼 핸들링

폼 핸들링은 데이터가 값이 변경되거나 전송될 때 데이터를 처리하는 방법에 대한 것입니다.

HTML에서 양식 데이터는 일반적으로 DOM에 의해 처리됩니다.

React에서 폼 데이터는 일반적으로 컴포넌트에 의해 처리됩니다.

데이터가 컴포넌트에서 처리되면 모든 데이터가 컴포넌트 ```state```로 저장됩니다.

```onChange``` 속성에 이벤트 핸들러를 추가하여 변경을 제어할 수 있습니다.

```useState``` Hook을 사용하여 각 입력값을 추적하고 애플리케이션 전체에 대해 "믿을 수 있는 단일 정보원"을 제공할 수 있습니다.

###### 예제 2 - ```useState``` Hook을 사용하여 입력을 관리합니다.

```javascript
import { useState } from "react";
import ReactDOM from 'react-dom';

function MyForm() {
  const [name, setName] = useState("");

  return (
    <form>
      <label>Enter your name:
        <input
          type="text" 
          value={name}
          onChange={(e) => setName(e.target.value)}
        />
      </label>
    </form>
  )
}

ReactDOM.render(<MyForm />, document.getElementById('root'));
```

## 폼 제출

submit 액션을 제어하려면 다음의 ```<form>```의 ```onSubmit``` 속성에 이벤트핸들러를 추가합니다.

###### 예제 3 - ```onSubmit``` 속성에 Submit 버튼과 이벤트핸들러를 추가합니다.

```javascript
import { useState } from "react";
import ReactDOM from 'react-dom';

function MyForm() {
  const [name, setName] = useState("");

  const handleSubmit = (event) => {
    event.preventDefault();
    alert(`The name you entered was: ${name}`)
  }

  return (
    <form onSubmit={handleSubmit}>
      <label>Enter your name:
        <input 
          type="text" 
          value={name}
          onChange={(e) => setName(e.target.value)}
        />
      </label>
      <input type="submit" />
    </form>
  )
}

ReactDOM.render(<MyForm />, document.getElementById('root'));
```

## 다중 입력 필드

각 요소에 ```name``` 속성을 추가하여 여러 입력 필드의 값을 제어할 수 있습니다.

빈 객체로 상태를 초기화합니다.

이벤트 핸들러의 필드에 액세스하려면 ```event.target.name``` 및 ```event.target.value``` 구문을 사용합니다.

상태를 업데이트하려면 속성 이름 주위에 대괄호 "브래킷 표기"를 사용합니다.

###### 예제 4 - 2개의 입력 필드가 있는 폼을 작성합니다.

```javascript
import { useState } from "react";
import ReactDOM from "react-dom";

function MyForm() {
  const [inputs, setInputs] = useState({});

  const handleChange = (event) => {
    const name = event.target.name;
    const value = event.target.value;
    setInputs(values => ({...values, [name]: value}))
  }

  const handleSubmit = (event) => {
    event.preventDefault();
    alert(inputs);
  }

  return (
    <form onSubmit={handleSubmit}>
      <label>Enter your name:
      <input 
        type="text" 
        name="username" 
        value={inputs.username || ""} 
        onChange={handleChange}
      />
      </label>
      <label>Enter your age:
        <input 
          type="number" 
          name="age" 
          value={inputs.age || ""} 
          onChange={handleChange}
        />
        </label>
        <input type="submit" />
    </form>
  )
}

ReactDOM.render(<MyForm />, document.getElementById('root'));
```

{: .box-note}
양쪽 입력 필드에 동일한 이벤트핸들러 함수를 사용하여 각 필드에 1개의 이벤트핸들러를 쓸 수 있고, 이것은 보다 깨끗한 코드를 얻을 수 있어 리액트에서는 권장되는 방법입니다.

## textarea

React의 ```textarea``` 요소는 일반 HTML과 약간 다릅니다.

HTML에서 ```textarea```의 값은 시작 태그 ```<textarea>```와 끝 태그 ```</textarea>``` 사이의 텍스트입니다.

```html
<textarea>
  Content of the textarea.
</textarea>
```

React에서 ```textarea```의 값은 ```value``` 속성에 배치됩니다. ```useState``` Hook을 사용하여 텍스트 영역의 값을 관리합니다.

###### 예제 5 - 일부 내용이 포함된 단순한 텍스트 영역

```javascript
import { useState } from "react";
import ReactDOM from "react-dom";

function MyForm() {
  const [textarea, setTextarea] = useState(
    "The content of a textarea goes in the value attribute"
  );

  const handleChange = (event) => {
    setTextarea(event.target.value)
  }

  return (
    <form>
      <textarea value={textarea} onChange={handleChange} />
    </form>
  )
}

ReactDOM.render(<MyForm />, document.getElementById('root'));
```

## Select

React의 drop down list 또는 select box도 HTML과 조금 다릅니다.

HTML에서는 drop down list에서 선택한 값이 ```selected``` 속성으로 정의되었습니다.

```html
<select>
  <option value="Ford">Ford</option>
  <option value="Volvo" selected>Volvo</option>
  <option value="Fiat">Fiat</option>
</select>
```

React에서 선택한 값은 ```select``` 태그의 ```value``` 속성으로 정의됩니다.

###### 예제 6 - 단순 선택 상자에서 선택한 값 "Volvo"가 생성자에서 초기화됩니다.

```javascript
function MyForm() {
  const [myCar, setMyCar] = useState("Volvo");

  const handleChange = (event) => {
    setMyCar(event.target.value)
  }

  return (
    <form>
      <select value={myCar} onChange={handleChange}>
        <option value="Ford">Ford</option>
        <option value="Volvo">Volvo</option>
        <option value="Fiat">Fiat</option>
      </select>
    </form>
  )
}
```

React는 ```<textarea>```와 ```<select>```를 약간 변경함으로써 모든 입력 요소를 동일하게 처리할 수 있습니다.
