---
layout: post
title: HTML 50. 웹 워커 API (Web Workers API)
subtitle: 웹 워커는 페이지의 성능에 영향을 주지 않고 백그라운드에서 실행되는 JavaScript입니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<a href="https://youtu.be/apl8TKlEHTM" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 50. 웹 워커 API (Web Workers API) 영상 보러가기</a>
<br>
<br>

# HTML 웹 워커 API

## 웹 워커란?

HTML 페이지에서 스크립트를 실행하면 스크립트가 완료될 때까지 페이지가 응답하지 않습니다.

웹 워커는 페이지의 성능에 영향을 주지 않고 다른 스크립트와 독립적으로 백그라운드에서 실행되는 JavaScript입니다. 웹 워커가 백그라운드에서 실행되는 동안 클릭, 선택 등 원하는 작업을 계속할 수 있습니다.

## 지원 브라우저

표의 숫자는 웹 워커를 완전히 지원하는 최소 브라우저 버전을 지정합니다.

| 브라우저 | 구글 Chrome | 마이크로소프트 Edge | Firefox | Safari | Opera |
| 버전 | 4.0 | 10.0 | 3.5 | 4.0 | 11.5 |

## 웹 워커 지원 확인

웹 워커를 작성하기 전에 사용자의 브라우저가 웹 워커를 지원하는지 확인합니다.

```javascript
if (typeof(Worker) !== "undefined") {
  // 웹워커 지원
} else {
  // 웹워커 미지원
}
```

## 웹 워커 파일 생성

이제 외부 JavaScript에서 웹 워커를 생성해 보겠습니다.

여기서는 카운트하는 스크립트를 만듭니다. 스크립트는 "demo_workers.js" 파일에 저장됩니다.

```javascript
var i = 0;

function timedCount() {
  i = i + 1;
  postMessage(i);
  setTimeout("timedCount()",500);
}

timedCount();
```

위의 코드에서 중요한 부분은 ```postMessage()``` 메서드입니다. 이것은 메시지를 HTML 페이지에 다시 게시하기 위해 사용됩니다.

{: .box-note}
일반적으로 웹 워커는 이러한 단순한 스크립트가 아니라 CPU를 많이 사용하는 작업에 사용됩니다.

## 웹 워커 객체 생성

이제 웹 워커 파일을 얻었으니 HTML 페이지에서 호출해야 합니다.

다음 행은 워커가 이미 존재하는지 여부를 확인합니다. 존재하지 않는 경우 새로운 웹 워커 객체를 생성하여 "demo_workers.js" 코드를 실행합니다.

```javascript
if (typeof(w) == "undefined") {
  w = new Worker("demo_workers.js");
}
```

그러면 웹 워커와 메시지를 주고받을 수 있습니다.

웹 워커에 "onmessage" 이벤트 리스너를 추가합니다.

```javascript
w.onmessage = function(event){
  document.getElementById("result").innerHTML = event.data;
};
```

웹 워커가 메시지를 게시하면 이벤트 리스너 내의 코드가 실행됩니다. 웹 워커의 데이터는 ```event.data```에 저장됩니다.

## 웹 워커 종료

웹 워커 오브젝트가 생성되면 (외부 스크립트가 종료된 후에도) 종료될 때까지 메시지를 계속 수신합니다.

웹 워커를 종료하고 브라우저/컴퓨터 리소스를 해제하려면 ```terminate()``` 메서드를 사용합니다.

```javascript
w.terminate();
```

## 웹 워커 재사용

```worker``` 변수를 ```undefined```로 설정하면 종료 후 코드를 재사용할 수 있습니다.

## 웹 워커의 전체 코드 예시

```html
<!DOCTYPE html>
<html>
<body>

<p>Count numbers: <output id="result"></output></p>
<button onclick="startWorker()">Start Worker</button>
<button onclick="stopWorker()">Stop Worker</button>

<script>
var w;

function startWorker() {
  if (typeof(Worker) !== "undefined") {
    if (typeof(w) == "undefined") {
      w = new Worker("demo_workers.js");
    }
    w.onmessage = function(event) {
      document.getElementById("result").innerHTML = event.data;
    };
  } else {
    document.getElementById("result").innerHTML = "Sorry! No Web Worker support.";
  }
}

function stopWorker() {
  w.terminate();
  w = undefined;
}
</script>

</body>
</html>
```

## 웹 워커와 DOM

웹 워커는 외부 파일에 있으므로 다음 javaScript 객체에 액세스할 수 없습니다.

+ window 객체
+ document 객체
+ parent 객체
