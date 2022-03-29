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
