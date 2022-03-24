---
layout: post
title: React 01. 소개
subtitle: React 소개
cover-img: /assets/img/react_img.png
thumbnail-img: /assets/img/react_thumb.png
share-img: /assets/img/react_img.png
tags: [React.js, basic]
---

# React 소개

## 리액트란?

프론트엔드 JavaScript 프레임워크라고도 불리는 리액트는 Facebook에 의해 작성된 JavaScript 라이브러리입니다.

React는 UI 컴포넌트를 빌드하기 위한 도구입니다.

## 리액트는 어떻게 동작하는가?

{: .box-note}
React는 메모리에 가상 DOM을 생성합니다.

브라우저의 DOM을 직접 조작하는 대신 React는 메모리 내에 가상 DOM을 생성하여 필요한 조작을 모두 수행한 후 브라우저 DOM을 변경합니다.

{: .box-note}
리액트는 변경해야 할 부분만 변경합니다!

React는 어떤 변경이 이루어졌는지 파악하여 **변경해야 할 사항만** 변경합니다.

이 튜토리얼의 나머지 부분에서는 React가 이를 수행하는 방법에 대한 다양한 측면에 대해 설명합니다.

## React.js 역사

React.JS는의 현재 버전 V17.0.2(2021년 8월)입니다.

최초 공개(V0.3.0)는 2013년 7월에 공개되었습니다.

React.JS는 페이스북의 뉴스피드 기능을 위해 2011년에 처음 사용되었습니다.

Facebook 소프트웨어 엔지니어 Jordan Walke가 만들었습니다.

```create-react-app``` 의 현재 버전은 v4.0.3(2021년 8월)입니다.

```create-react-app``` 에는 웹 팩, Babel, ESLint 등의 빌드 도구가 포함되어 있습니다.
