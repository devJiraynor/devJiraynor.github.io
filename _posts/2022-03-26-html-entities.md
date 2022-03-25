---
layout: post
title: HTML 29. 엔티티 (Entities)
subtitle: HTML의 예약된 문자는 문자 엔티티로 대체해야 합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

# HTML 엔티티

## HTML 엔티티

일부 문자는 HTML로 예약되어 있습니다.

텍스트에서 작거나 (<) 큰 (>) 부호를 사용하면 브라우저가 이러한 부호를 태그와 함께 사용할 수 있습니다.

문자 엔티티요소는 HTML에서 예약된 문자를 표시하는 데 사용됩니다.

문자 엔티티요소는 다음과 같습니다.

```html
&entity_name;
OR

&#entity_number;
```

미만 기호(<)를 표시하려면 다음과 같이 입력해야 합니다. ```&lt;``` 또는 ```&#60;```

{: .box-note}
**엔티티 이름을 사용하는 장점**: 엔티티 이름은 기억하기 쉽습니다.

{: .box-note}
**엔티티 이름 사용의 단점**: 브라우저가 모든 엔티티 이름을 지원하는 것은 아니지만 엔티티 번호에 대한 지원은 양호합니다.

## Non-breaking Space

HTML에서 일반적으로 사용되는 엔티티는 띄어쓰기 (```&nbsp;```)입니다: 

Non-breaking Space은 새 행에 끼어들지 않는 공간입니다.

공백 없이 구분된 두 단어가 서로 붙습니다(새 행으로 구분되지 않음). 이것은 단어를 깨질수 있는 경우에 편리합니다.

+ § 10
+ 10 km/h
+ 10 PM

또한 브라우저가 HTML 페이지의 공간을 잘라내지 않도록 하는 것도 일반적인 방법입니다.

텍스트에 공백 10개를 입력하면 브라우저는 그 중 9개를 삭제합니다. 텍스트에 실제 공간을 추가하려면 ```&nbsp;``` 문자 엔티티를 사용할 수 있습니다.

{:. box-note}
**Tip:** non-breaking hyphen(&#8209;)은 새 줄로 non-breaking hyphen(-)을 정의하는 데 사용됩니다.

## 유용한 HTML 문자 엔티티

| 결과 | 설명 | 엔티티 이름 | 엔티티 번호 |
| &nbsp; | 공백 | ```&nbsp;``` | ```&#160``` |
