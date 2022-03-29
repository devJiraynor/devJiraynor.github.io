---
layout: post
title: HTML 47. 지리 위치 API (Geolocation API)
subtitle: HTML Geolocation API는 사용자의 위치를 찾기 위해 사용됩니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 지리 위치 API

## 사용자 위치 찾기

HTML Geolocation API는 사용자의 지리적 위치를 얻기 위해 사용됩니다.

이로 인해 사생활이 침해될 수 있기 때문에 사용자가 승인하지 않으면 이 기능을 사용할 수 없습니다.

{: .box-note}
**Note:**  GPS를 탑재한 기기(예: 스마트폰)에서 지리정보가 가장 정확합니다.

## 지원 브라우저

표의 숫자는 Geolocation을 완전히 지원하는 최소 브라우저 버전을 지정합니다.

| 브라우저 | 구글 Chrome | 마이크로소프트 Edge | Firefox | Safari | Opera |
| 버전 | 5.0 - 49.0 (http)<br>50.0 (https) | 9.0 | 3.5 | 5.0 | 16.0 |

{: .box-note}
**Note:** Chrome 50에서 Geolocation API는 HTTPS와 같은 보안 컨텍스트에서만 작동합니다. 사이트가 비보안 원본(HTTP 등)에서 호스팅되는 경우 사용자 위치를 가져오는 요청은 더 이상 작동하지 않습니다.

## HTML 지리 위치 사용

```getCurrentPosition()``` 메서드는 사용자의 위치를 반환하기 위해 사용됩니다.

다음 예제에서는 사용자 위치의 위도와 경도를 반환합니다.

###### 예제 1

```html
<script>
var x = document.getElementById("demo");
function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(showPosition);
  } else {
    x.innerHTML = "Geolocation is not supported by this browser.";
  }
}

function showPosition(position) {
  x.innerHTML = "Latitude: " + position.coords.latitude +
  "<br>Longitude: " + position.coords.longitude;
}
</script>
```

예제 설명 : 

+ Geolocation이 지원되는지 확인합니다.
+ 지원되는 경우 ```getCurrentPosition()``` 메서드를 실행합니다. 그렇지 않은 경우 사용자에게 메시지를 표시합니다.
+ ```getCurrentPosition()``` 메서드가 성공하면 파라미터(```showPosition```)로 지정된 함수로 좌표 객체가 반환됩니다.
+ ```showPosition()``` 함수는 위도와 경도를 출력합니다.

## 오류 및 거부 처리

getCurrentPosition() 메서드의 두 번째 파라미터는 오류 처리에 사용됩니다. 사용자 위치를 가져오지 못한 경우 실행할 함수를 지정합니다.

###### 예제 2

```html
function showError(error) {
  switch(error.code) {
    case error.PERMISSION_DENIED:
      x.innerHTML = "User denied the request for Geolocation."
      break;
    case error.POSITION_UNAVAILABLE:
      x.innerHTML = "Location information is unavailable."
      break;
    case error.TIMEOUT:
      x.innerHTML = "The request to get user location timed out."
      break;
    case error.UNKNOWN_ERROR:
      x.innerHTML = "An unknown error occurred."
      break;
  }
}
```

## 로케이션 고유의 정보

지도에 사용자의 위치를 표시하는 방법을 시연했습니다.

지리 로케이션은 다음과 같은 로케이션 고유의 정보에도 매우 편리합니다.

+ 최신 지역 정보
+ 사용자 근처에 관심 지점 표시
+ 턴 바이 턴 내비게이션(GPS)

## ```getCurrentPosition()``` 메서드 - 데이터 반환

```getCurrentPosition()``` 메서드는 성공 시 객체를 반환합니다. 위도, 경도 및 정확도 속성은 항상 반환됩니다. 사용 가능한 경우 다른 속성이 반환됩니다.

| 속성 | 반환 |
| coords.latitude | 10진수로서의 위도(항상 반환) |
| coords.longitude | 10진수로서의 경도(항상 반환) |
| coords.accuracy | 위치 정확도(항상 반환) |
| coords.altitude | 평균 고도(m)(사용 가능한 경우 반환) |
| coords.altitudeAccuracy | 위치의 고도 정확도(사용 가능한 경우 반환) |
| coords.heading | 북 기준 시계방향으로 도 단위 방향(사용 가능한 경우 반환 |
| coords.speed | 속도(미터/초)(사용 가능한 경우 반환) |
| timestamp | 응답 날짜/시간(사용 가능한 경우 반환됨) |

## Geolocation 객체 - 기타 대상 메서드

Geolocation 객체에는 다른 메서드도 있습니다.

+ ```watchPosition()``` - 사용자의 현재 위치를 반환하고 사용자가 이동할 때 업데이트된 위치를 계속 반환합니다(차량 내 GPS 등).
+ ```clearWatch()``` - ```watchPosition()``` 메서드를 중지합니다.

###### 예제 3

```html
<script>
var x = document.getElementById("demo");
function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.watchPosition(showPosition);
  } else {
    x.innerHTML = "Geolocation is not supported by this browser.";
  }
}
function showPosition(position) {
  x.innerHTML = "Latitude: " + position.coords.latitude +
  "<br>Longitude: " + position.coords.longitude;
}
</script>
```
