---
layout: post
title: CSS 41. 특이도 (Specificity) - 우선순위
subtitle: 동일한 요소를 가리키는 CSS 규칙이 두 개 이상일 경우 처리 결과에 대해 알아봅니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 특이도 (Specificity)

## 특이도란?

동일한 요소를 가리키는 CSS 규칙이 두 개 이상일 경우, 가장 높은 특이도 값을 가진 셀렉터가 "우승"하며, 스타일 선언이 해당 HTML 요소에 적용될 것입니다.

특수성을 요소에 최종적으로 적용할 스타일 선언을 결정하는 점수/순위로 간주합니다.

###### 예제 1 - "p" 요소를 셀렉터로 사용하고 이 요소에 대한 빨간색 색상을 지정했습니다. 텍스트는 빨간색으로 표시됩니다.

```html
<html>
<head>
  <style>
    p {color: red;}
  </style>
</head>
<body>

<p>Hello World!</p>

</body>
</html>
```

###### 예제 2 - 이 예에서는 클래스 선택기("test")를 추가하고 이 클래스에 대해 녹색을 지정했습니다. 요소 선택기 "p"에 빨간색 색상을 지정했음에도 불구하고 텍스트가 녹색이 됩니다. 이는 클래스 선택기에 더 높은 우선 순위가 부여되기 때문입니다.
