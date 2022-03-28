---
layout: post
title: HTML 08. 인용 및 인용 요소 (Quotation and Citation Elements)
subtitle: 이 장에서는 block quote, q, abbr, address, cite 및 bdo HTML 요소에 대해 설명합니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/FscdpNx1uwA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<a href="https://youtu.be/FscdpNx1uwA" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 08. 인용 및 인용 요소 (Quotation and Citation Elements)</a>
<br>
<br>

# HTML 인용 및 인용 요소

## HTML 인용문 ```<blockquote>```

HTML ```<blockquote>``` 요소는 다른 소스에서 인용된 섹션을 정의합니다.

브라우저는 보통 ```<blockquote>``` 요소를 들여씁니다.

###### 예제 1

```html
<p>다음은 WWF 웹사이트에서 인용한 내용입니다:</p>
<blockquote cite="http://www.worldwildlife.org/who/index.html">
50년 동안, WWF는 자연의 미래를 지켜왔다.
세계 최고의 자연보호단체인
WWF는 100개국에서 운용되며 다음 지원 대상입니다.
120만 명의 미국 회원과
전 세계적으로 500만 명에 육박합니다.
</blockquote>
```

## HTML 짧은 인용문 ```<q>```

HTML ```<q>``` 태그는 짧은 따옴표를 정의합니다.

브라우저는 보통 따옴표를 삽입합니다.
  
###### 예제 2

```html
<p>WWF의 목표: <q>사람들이 자연과 조화를 이루며 사는 미래를 건설한다.</q></p>
```
  
## HTML 약어 ```<abbr>```
  
HTML ```<abbr>``` 태그는 "HTML", "CSS", "Mr", "Dr", "ASAP", "ATM" 등의 두문자어 또는 축약어를 정의합니다.

약어는 브라우저, 번역 시스템 및 검색 엔진에 유용한 정보를 제공할 수 있습니다.
  
{: .box-note}
**Tip:** 요소를 마우스로 가리킬 때 약어/두문자어에 대한 설명을 표시하려면 글로벌 title 속성을 사용합니다.
  
###### 예제 3
  
```html
<p><abbr title="World Health Organization">WHO</abbr>는 1948년에 설립되었습니다.</p>
```

## HTML 연락처 정보 ```<address>```
  
HTML ```<address>``` 태그는 문서 또는 문서의 작성자/소유자의 연락처 정보를 정의합니다.

연락처 정보는 이메일 주소, URL, 실제 주소, 전화번호, 소셜 미디어 핸들 등입니다.

```<address>``` 요소의 텍스트는 보통 이탤릭체로 렌더링되며 브라우저는 항상 ```<address>``` 요소의 앞뒤에 줄 바꿈을 추가합니다.
  
###### 예제 4
  
```html
<address>
작성자 : Jiraynor <br>
email 주소 : <br>
lacls159@gmail.com <br>
github blog : <br>
devJiraynor.github.io
</address>
```
  
## HTML 작업 제목 ```<cite>```

HTML ```<cite>``` 태그는 창작물(책, 시, 노래, 영화, 그림, 조각 등)의 제목을 정의합니다.
  
{: .box-note}
**Note:** 사람의 이름은 작품의 제목이 아닙니다.
  
```<cite>``` 요소의 텍스트는 보통 이탤릭체로 렌더링됩니다.
  
###### 예제 5

```html
<p>몽크의 <cite>절규</cite>. 1893년 작.</p>
```
  
## HTML 역정렬 ```<bdo>```

BDO는 Bi-Directional Override의 약자입니다.

HTML ```<bdo>``` 태그는 현재 텍스트를 역방향으로 표시하기 위해 사용됩니다.
  
###### 예제 6

```html
<bdo dir="rtl">이 텍스트는 오른쪽에서 왼쪽으로 작성되어집니다.</bdo>
```
