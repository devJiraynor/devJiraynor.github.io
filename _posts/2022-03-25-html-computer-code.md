---
layout: post
title: HTML 26. 컴퓨터 코드 (Computer Code)
subtitle: HTML에는 사용자 입력 및 컴퓨터 코드를 정의하기 위한 몇 가지 요소가 포함되어 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/8dFGvMRk5-E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<a href="https://youtu.be/8dFGvMRk5-E" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 26. 컴퓨터 코드 (Computer Code)</a>
<br>
<br>

# HTML 컴퓨터 코드 요소

## HTML 키보드 입력 ```<kbd>``` 요소

HTML ```<kbd>``` 요소는 키보드 입력 정의에 사용됩니다. 내부 내용은 브라우저의 기본 monospace 글꼴로 표시됩니다.

###### 예제 1

```html
<p>Save the document by pressing <kbd>Ctrl + S</kbd></p>
```

## HTML 프로그램 출력 ```<samp>``` 요소

HTML ```<samp>``` 요소는 컴퓨터 프로그램에서 샘플 출력을 정의하기 위해 사용됩니다. 내부 내용은 브라우저의 기본 monospace 글꼴로 표시됩니다.

###### 예제 2

```html
<p>Message from my computer:</p>
<p><samp>File not found.<br>Press F1 to continue</samp></p>
```

## HTML 컴퓨터 코드 ```<code>``` 요소

HTML ```<code>``` 요소는 컴퓨터 코드의 일부를 정의하기 위해 사용됩니다. 내부 내용은 브라우저의 기본 monospace 글꼴로 표시됩니다.

###### 예제 3

```html
<code>
x = 5;
y = 6;
z = x + y;
</code>
```

```<code>``` 요소는 여분의 공백과 줄 바꿈을 유지하지 않습니다.

이 문제를 해결하려면 ```<code>``` 요소를 ```<pre>``` 요소 안에 넣습니다.

###### 예제 4

```html
<pre>
<code>
x = 5;
y = 6;
z = x + y;
</code>
</pre>
```

## HTML 변수 ```<var>```

HTML ```<var>``` 요소는 프로그래밍 또는 수학식으로 변수를 정의하기 위해 사용됩니다. 내용물은 일반적으로 이탤릭체로 표시됩니다.

###### 예제 5

```html
<p>The area of a triangle is: 1/2 x <var>b</var> x <var>h</var>, where <var>b</var> is the base, and <var>h</var> is the vertical height.</p>
```

## Summary

+ ```<kbd>``` 요소는 키보드 입력을 정의합니다.
+ ```<samp>``` 요소는 컴퓨터 프로그램의 샘플 출력을 정의합니다.
+ ```<code>``` 요소는 컴퓨터 코드의 일부를 정의합니다.
+ ```<var>``` 요소는 프로그래밍 또는 수학식으로 변수를 정의합니다.
+ ```<pre>``` 요소는 미리 포맷된 텍스트를 정의합니다.
