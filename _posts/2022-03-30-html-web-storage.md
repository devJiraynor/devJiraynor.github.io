---
layout: post
title: HTML 49. 웹 스토리지 API (Web Storage API)
subtitle: HTML 웹 스토리지로 쿠키보다 우수합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 웹 스토리지 API

## HTML 웹 스토리지 란?

웹 스토리지를 사용하면 웹 애플리케이션은 사용자의 브라우저 내에 로컬로 데이터를 저장할 수 있습니다.

HTML5 이전에는 모든 서버 요청에 포함된 쿠키에 애플리케이션 데이터를 저장해야 했습니다. 웹 스토리지는 보다 안전하며 웹 사이트의 성능에 영향을 주지 않고 많은 양의 데이터를 로컬로 저장할 수 있습니다.

쿠키와 달리 저장공간은 훨씬 더 크고(5MB 이상) 정보는 서버로 전송되지 않습니다.

웹 스토리지는 원본 별(도메인별 및 프로토콜별)입니다. 모든 페이지는 하나의 원본에서 동일한 데이터를 저장하고 액세스할 수 있습니다.

## 지원 브라우저

표의 숫자는 웹 스토리지를 완전히 지원하는 최소 브라우저 버전을 지정합니다.

| 브라우저 | 구글 Chrome | 마이크로소프트 Edge | Firefox | Safari | Opera |
| 버전 | 4.0 | 8.0 | 3.5 | 4.0 | 11.5 |

## HTML 웹 스토리지 객체

HTML 웹 스토리지는 클라이언트에 데이터를 저장하기 위한 두 가지 객체를 제공합니다.

+ ```window.localStorage``` - 만료일 없이 데이터를 저장합니다.
+ ```window.session Storage``` - 한 세션의 데이터를 저장합니다(브라우저 탭을 닫으면 데이터가 손실됩니다).

웹 저장소를 사용하기 전에 ```localStorage``` 및 ```sessionStorage```에 대한 브라우저 지원을 확인하십시오.

```javascript
if (typeof(Storage) !== "undefined") {
  // localStorage/sessionStorage 사용 코드
} else {
  // 브라우저에서 localStorage/sessionStorage 를 지원하지 않을때
}
```

## ```localStorage``` 객체

```localStorage``` 객체는 만료 날짜 없이 데이터를 저장합니다. 브라우저가 닫혀도 데이터는 삭제되지 않고 다음 날, 다음 주 또는 다음 해에도 사용할 수 있습니다.

```javascript
// Store
localStorage.setItem("lastname", "Smith");

// Retrieve
document.getElementById("result").innerHTML = localStorage.getItem("lastname");
```

예제 설명:

+ ```name="lastname"``` 및 ```value="Smith"```를 사용하여 ```localStorage``` 이름/값 쌍 생성
+ ```"lastname"``` 값을 검색하여 ```id="result"```인 요소에 삽입합니다.

위의 예는 다음과 같이 작성할 수도 있습니다.

```javascript
// Store
localStorage.lastname = "Smith";
// Retrieve
document.getElementById("result").innerHTML = localStorage.lastname;
```

"lastname"을 ```localStorage```에서 삭제하는 구문은 다음과 같습니다.

```javascript
localStorage.removeItem("lastname");
```

{: .box-note}
이름/값 쌍은 항상 문자열로 저장됩니다. 필요할 때 다른 형식으로 변환해야 합니다.

다음 예제에서는 사용자가 버튼을 클릭한 횟수를 카운트합니다. 이 코드에서는 카운터를 늘릴 수 있도록 값 문자열이 숫자로 변환됩니다.

```javascript
if (localStorage.clickcount) {
  localStorage.clickcount = Number(localStorage.clickcount) + 1;
} else {
  localStorage.clickcount = 1;
}
document.getElementById("result").innerHTML = "You have clicked the button " +
localStorage.clickcount + " time(s).";
```

## ```sessionStorage``` 객체

```sessionStorage``` 객체는 ```localStorage``` 객체와 동일하지만 한 세션의 데이터만 저장합니다. 사용자가 특정 브라우저 탭을 닫으면 데이터가 삭제됩니다.

다음 예제에서는 현재 세션에서 사용자가 버튼을 클릭한 횟수를 카운트합니다.

```javascript
if (sessionStorage.clickcount) {
  sessionStorage.clickcount = Number(sessionStorage.clickcount) + 1;
} else {
  sessionStorage.clickcount = 1;
}
document.getElementById("result").innerHTML = "You have clicked the button " +
sessionStorage.clickcount + " time(s) in this session.";
```
