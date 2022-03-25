---
layout: post
title: HTML 32. 인코딩 (Encoding)
subtitle: HTML 페이지를 올바르게 표시하려면 웹 브라우저가 사용할 문자 집합을 알아야 합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 인코딩 (문자셋)

## ASCII에서 UTF-8로

ASCII는 최초의 문자 부호화 표준이었습니다. ASCII는 인터넷상에서 사용할 수 있는 128개의 다른 문자(0-9), 영문자(A-Z), 및!$ + - ( ) @ < > 등의 특수 문자를 정의했습니다.

ISO-8859-1 은 HTML4 의 기본 문자셋입니다. 이 문자셋은 256개의 다른 문자 코드를 지원했습니다. HTML4는 UTF-8도 지원했습니다.

ANSI(Windows-1252)는 원래의 Windows 문자 세트입니다. ANSI는 ISO-8859-1과 동일하지만 ANSI에 32자가 추가되어 있습니다.

HTML5 사양은 웹 개발자들에게 UTF-8 문자셋을 사용하도록 권장하고 있습니다. UTF-8 문자셋은 전 세계의 거의 모든 문자와 기호를 포함합니다.

## HTML 문자셋 속성

HTML 페이지를 올바르게 표시하려면 웹 브라우저가 페이지에서 사용되는 문자 집합을 알아야 합니다.

이것은 <meta>태그에 지정되어 있습니다.

```html
<meta charset="UTF-8">
```

## ASCII 문자셋

ASCII는 제어 문자에 0 ~31(및 127)의 값을 사용합니다.

ASCII는 문자, 숫자 및 기호로 32 ~126 의 값을 사용합니다.

ASCII 에서는 128 ~255 의 값은 사용되지 않습니다.

## ANSI (Window-1252) 문자셋

ANSI는 0 ~127의 값에 대해 ASCII와 동일합니다.

ANSI 에는 128 ~159 의 값의 독자적인 문자 세트가 있습니다.

ANSI는 160 ~255의 값으로 UTF-8과 동일합니다.

## ISO-8859-1 문자셋

ISO-8859-1은 0 ~127의 값의 ASCII와 동일합니다.

ISO-8859-1에서는 128 ~159 의 값은 사용되지 않습니다.

ISO-8859-1은 160 ~255의 값으로 UTF-8과 동일합니다.

## UTF-8 문자셋

UTF-8은 0 ~127의 값의 ASCII와 동일합니다.

UTF-8 에서는 128 ~159 의 값은 사용되지 않습니다.

UTF-8은 160 ~255의 값으로 ANSI 및 8859-1과 동일합니다.

UTF-8은 값 256에서 10,000자를 넘는 다른 문자로 계속됩니다.
