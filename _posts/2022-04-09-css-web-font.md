---
layout: post
title: CSS 52. 웹 글꼴 (Web Font)
subtitle: CSS 웹 글꼴 사용방법에 대해 알아봅니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 웹 글꼴

## @font-face 규칙

웹 글꼴을 사용하면 웹 설계자가 사용자의 컴퓨터에 설치되지 않은 글꼴을 사용할 수 있습니다.

사용할 글꼴을 찾거나 구입했으면 웹 서버에 글꼴 파일만 포함하면 필요할 때 자동으로 사용자에게 다운로드됩니다.

"소유한" 글꼴은 ```@font-face``` 규칙 내에 정의됩니다.

## 글꼴 형식 차이

**TrueType Fonts (TTF)**

트루타입(TrueType)은 1980년대 말 애플과 마이크로소프트가 개발한 글꼴 표준입니다. 트루타입은 맥 OS와 마이크로소프트 윈도우 운영 체제에서 가장 일반적인 글꼴 형식입니다.

**OpenType Fonts (OTF)**

OpenType은 확장 가능한 컴퓨터 글꼴을 위한 형식입니다. 트루타입에 기반을 두고 있으며 마이크로소프트의 등록 상표입니다. OpenType 글꼴은 오늘날 주요 컴퓨터 플랫폼에서 일반적으로 사용됩니다.

**The Web Open Font Format (WOFF)**

WOFF는 웹 페이지에서 사용하는 글꼴 형식입니다. 2009년에 개발되었으며, 현재는 W3C 권장 사항입니다. WOFF는 기본적으로 압축과 추가 메타데이터가 있는 OpenType 또는 TrueType입니다. 목표는 대역폭 제약이 있는 네트워크를 통해 서버에서 클라이언트로 글꼴 배포를 지원하는 것입니다.

**The Web Open Font Format (WOFF 2.0)**

WOFF 1.0보다 더 나은 압축을 제공하는 TrueType/OpenType 글꼴입니다.

**SVG Fonts/Shapes**

SVG 글꼴을 사용하면 텍스트를 표시할 때 SVG를 글리프로 사용할 수 있습니다. SVG 1.1 사양은 SVG 문서 내에서 글꼴을 만들 수 있는 글꼴 모듈을 정의합니다. 또한 CSS를 SVG 문서에 적용할 수 있으며 @font-face 규칙을 SVG 문서의 텍스트에 적용할 수 있습니다.

**Embedded OpenType Fonts (EOT)**

EOT 글꼴은 마이크로소프트가 웹 페이지에 내장된 글꼴로 사용하기 위해 설계한 오픈타입 글꼴의 간단한 형태입니다.

## 지원 브라우저

표의 숫자는 글꼴 형식을 완전히 지원하는 최소 브라우저 버전을 지정합니다.

| Font format | 구글 Chrome | 마이크로소프트 Edge | Firefox | Safari | Opera |
| TTF/OTF | 4.0 | 9.0 | 3.5 | 3.1 | 10.0 |
| WOFF | 5.0 | 9.0 | 3.6 | 5.1 | 11.1 |
| WOFF2 | 36.0 | 14.0 | 39.0 | 10.0 | 26.0 |
| SVG | 미지원 | 미지원 | 미지원 | 3.2 | 미지원 |
| EOT | 미지원 | 6.0 | 미지원 | 미지원 | 미지원 |

IE: 글꼴 형식은 "설치 가능"으로 설정된 경우에만 작동합니다.

## 원하는 글꼴 사용

```@font-face``` 규칙에서 먼저 글꼴 이름을 정의한 다음 글꼴 파일을 가리킵니다.

{: .box-note}
**Tip:** URL에는 항상 소문자를 사용하십시오. 대문자는 IE에서 예기치 않은 결과를 초래할 수 있습니다.

HTML 요소에 글꼴을 사용하려면 글꼴 패밀리 속성을 통해 글꼴 이름을 참조합니다.

###### 예제 1

```css
@font-face {
  font-family: myFirstFont;
  src: url(sansation_light.woff);
}

div {
  font-family: myFirstFont;
}
```

## 굵은 글씨 사용

굵은 글씨를 사용하기 위해서는 ```@font-face``` 규칙에 굵은 글씨 텍스트에 대한 설명자 추가해야 합니다.

###### 예제 2

```css
@font-face {
  font-family: myFirstFont;
  src: url(sansation_bold.woff);
  font-weight: bold;
}
```

"sansation_bold.woff" 파일은 Sansation 글꼴의 굵은 글자를 포함하는 또 다른 글꼴 파일입니다.

브라우저는 글꼴 계열의 "myFirstFont" 텍스트가 굵게 렌더링될 때마다 이 기능을 사용합니다.

이렇게 하면 동일한 글꼴에 대해 많은 ```@font-face``` 규칙을 가질 수 있습니다.

