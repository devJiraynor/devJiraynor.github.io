---
layout: post
title: CSS 08. 테두리 (Borders)
subtitle: CSS 테두리 특성을 사용하여 요소의 테두리 스타일, 너비 및 색상을 지정할 수 있습니다.
cover-img: /assets/img/css_img.png
thumbnail-img: /assets/img/css_thumb.png
share-img: /assets/img/css_img.png
tags: [css3, basic]
---

# CSS 테두리

## CSS 테두리 스타일

```border-style``` 속성은 표시할 테두리 유형을 지정합니다.

다음 값이 허용됩니다.

+ ```dotted``` - 점선 테두리를 정의합니다.
+ ```dashed``` - 점선 테두리를 정의합니다.
+ ```solid``` - 실선 테두리를 정의합니다.
+ ```double``` - 이중 테두리를 정의합니다.
+ ```groove``` - 3D 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.
+ ```ridge``` - 3D 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.
+ ```inset``` - 3D 오록 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.
+ ```outset``` - 3D 볼목 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.
+ ```none``` - 테두리를 정의하지 않습니다.
+ ```hidden``` - 테두리를 숨깁니다.

###### 예제 1

```css
p.dotted {border-style: dotted;}
p.dashed {border-style: dashed;}
p.solid {border-style: solid;}
p.double {border-style: double;}
p.groove {border-style: groove;}
p.ridge {border-style: ridge;}
p.inset {border-style: inset;}
p.outset {border-style: outset;}
p.none {border-style: none;}
p.hidden {border-style: hidden;}
p.mix {border-style: dotted dashed solid double;}
```

<p style="border-style: dotted;">점선 테두리를 정의합니다.</p>
<p style="border-style: dashed;">점선 테두리를 정의합니다.</p>
<p style="border-style: solid;">실선 테두리를 정의합니다.</p>
<p style="border-style: double;">이중 테두리를 정의합니다.</p>
<p style="border-style: groove;">3D 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.</p>
<p style="border-style: ridge;">3D 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.</p>
<p style="border-style: inset;">3D 오목 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.</p>
<p style="border-style: outset;">3D 볼록 테두리를 정의합니다. 효과는 테두리 색 값에 따라 달라집니다.</p>
<p style="border-style: none;">테두리를 정의하지 않습니다.</p>
<p style="border-style: hidden;">테두리를 숨깁니다.</p>
<p style="border-style: dotted dashed solid double;">스타일을 섞습니다.</p>
