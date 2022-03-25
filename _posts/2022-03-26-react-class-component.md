---
layout: post
title: React 07. 클래스 컴포넌트 (Class Components)
subtitle: React 16.8 이전에는 Class 컴포넌트가 React 컴포넌트의 상태와 라이프 사이클을 추적할 수 있는 유일한 방법이었습니다. 함수 컴포넌트는 "state-less"로 간주되었습니다.
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React 클래스 컴포넌트

React 16.8 이전에는 Class 컴포넌트가 React 컴포넌트의 상태와 라이프 사이클을 추적할 수 있는 유일한 방법이었습니다. 함수 컴포넌트는 "state-less"로 간주되었습니다.

후크가 추가되어 함수 컴포넌트는 클래스 컴포넌트와 거의 동일합니다. 차이는 매우 작기 때문에 React에서 Class 컴포넌트를 사용할 필요가 없습니다.

함수 컴포넌트 요소를 선호하지만, 현재 React에서 클래스 컴포넌트를 제거할 계획은 없습니다.

이 섹션에서는 React에서 클래스 컴포넌트를 사용하는 방법에 대한 개요를 제공합니다.

## React 컴포넌트

컴포넌트는 독립된 재사용 가능한 코드 비트입니다. 이들은 JavaScript 함수와 동일한 목적을 수행하지만 단독으로 작동하며 ```render()``` 함수를 통해 HTML을 반환합니다.

컴포넌트는 클래스 컴포넌트와 함수 컴포넌트의 2가지 타입이 있습니다.이 장에서는 클래스 컴포넌트에 대해 설명합니다.

## 클래스 컴포넌트 생성

React 구성 요소를 생성할 때 구성 요소 이름은 대문자로 시작해야 합니다.

구성 요소는 ```extends React.Component``` 문을 포함해야 하며, 이 문은 ```React.Component```에 대한 상속을 생성하고 구성 요소에 ```React.Component``` 함수에 대한 액세스 권한을 부여합니다.

컴포넌트에는 render() 메서드도 필요합니다.이 메서드는 HTML을 반환합니다.
