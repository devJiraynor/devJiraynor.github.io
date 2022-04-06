---
layout: post
title: JavaScript 19. 문자열 검색 (String Search)
subtitle: 문자열 검색 메서드는 문자열에서 특정 문자열을 검색하는데 사용됩니다.
cover-img: /assets/img/js_img.png
thumbnail-img: /assets/img/js_thumb.png
share-img: /assets/img/js_img.png
tags: [javascript, basic]
---

# JavaScript 문자열 검색

## indexOf()

```indexOf()``` 메서드는 문자열에서 지정한 텍스트의 첫 번째 위치 인덱스를 반환합니다.

###### 예제 1

```javascript
let str = "Please locate where 'locate' occurs!";
str.indexOf("locate");
```

{: .box-note}
JavaScript는 0부터 위치를 계산합니다.<br>0은 문자열의 첫 번째 위치이고, 1은 두 번째, 2는 세 번째, ...

## lastIndexOf()

```lastIndexOf()``` 메서드는 문자열에서 지정한 텍스트의 **마지막** 인덱스를 반환합니다.

###### 예제 2

```javascript
let str = "Please locate where 'locate' occurs!";
str.lastIndexOf("locate");
```

텍스트를 찾을 수 없는 경우 ```indexOf()```와 ```lastIndexOf()``` 모두 -1을 반환합니다.

###### 예제 3

```javascript
let str = "Please locate where 'locate' occurs!";
str.lastIndexOf("John");
```

두 방법 모두 두 번째 매개 변수를 검색의 시작 위치로 사용할 수 있습니다.

###### 예제 4

```javascript
let str = "Please locate where 'locate' occurs!";
str.indexOf("locate", 15);
```

```lastIndexOf()``` 메서드는 두 번째 매개 변수가 15인 경우 위치 15에서 검색을 시작하여 문자열의 시작 부분까지 검색한다는 의미입니다.

###### 예제 5

```javascript
let str = "Please locate where 'locate' occurs!";
str.lastIndexOf("locate", 15);
```

## search()

```search()``` 메서드는 문자열에서 지정된 값을 검색하고 일치하는 위치를 반환합니다.

###### 예제 6

```javascript
let str = "Please locate where 'locate' occurs!";
str.search("locate");
```

## indexOf()와 search()의 차이점

두 가지 방법은 같지 않습니다. 차이점은 다음과 같습니다.

+ ```search()``` 메서드는 두 번째 시작 위치 인수를 사용할 수 없습니다.
+ ```indexOf()``` 메서드는 정규식을 사용할 수 없습니다.

## match()

```match()``` 메서드는 정규식과 일치하는 문자열을 검색하고 일치하는 항목을 배열 객체로 반환합니다.

###### 예재 7

```javascript
let text = "The rain in SPAIN stays mainly in the plain";
text.match(/ain/g);
```

{: .box-note}
정규식에 전역 검색을 수행하기 위해 g 수식자가 포함되지 않은 경우 ```match()``` 메서드는 문자열에서 첫 번째 일치 항목만 반환합니다.

## match() 구문

```javascript
string.match(regexp)
```

| regexp | 필수. 정규식으로 검색할 값입니다. |
| 반환값 | 일치 항목이 포함된 배열, 일치 항목마다 하나씩 또는 일치하는 항목이 없는 경우 null |

###### 예제 8

```javascript
let text = "The rain in SPAIN stays mainly in the plain";
text.match(/ain/gi);
```

## include()

```includes()``` 메서드는 문자열에 지정된 값이 포함된 경우 ```true```를 반환합니다.

###### 예제 9

```javascript
let text = "Hello world, welcome to the universe.";
text.includes("world");
```

## include() 구문

```javascript
string.includes(searchvalue, start)
```

| searchvalue | 필수. 검색할 문자열 |
| start | 선택. 기본값 0. 검색을 시작할 위치 |
| 반환값 | 문자열에 값이 포함되어 있으면 ```true```를 반환하고, 그렇지 않으면 ```false```를 반환합니다. |
| js 버전 | ES6 (2015) |

##### 예제 9

```javascript
let text = "Hello world, welcome to the universe.";
text.includes("world", 12);
```

## include() 지원 브라우저

```includes()```는 ES6 기능(JavaScript 2015)입니다).

모든 최신 브라우저에서 지원됩니다.

```includes()```는 Internet Explorer에서 지원되지 않습니다.

## startsWith()

```startsWith()``` 메서드는 문자열이 지정된 값으로 시작되면 ```true```를 반환하고, 그렇지 않으면 ```false```를 반환합니다.

###### 예제 10

```javascript
let text = "Hello world, welcome to the universe.";

text.startsWith("Hello");
```

## startsWith() 구문

```javascript
string.startsWith(searchvalue, start)
```

| searchvalue | 필수. 검색할 문자열 |
| start | 선택. 기본값 0. 검색을 시작할 위치 |

###### 예제 11

```javascript
let text = "Hello world, welcome to the universe.";

text.startsWith("world")    // false
```

```javascript
let text = "Hello world, welcome to the universe.";

text.startsWith("world", 5)    // false
```

```javascript
let text = "Hello world, welcome to the universe.";

text.startsWith("world", 6)    // true
```

{: .box-note}
```startsWith()``` 메서드는 대소문자를 구분합니다.

## startsWith() 지원 브라우저

```startsWith()```는 ES6 기능(JavaScript 2015)입니다.

모든 최신 브라우저에서 지원됩니다.

```startsWith()```는 Internet Explorer(인터넷 익스플로러)에서 지원되지 않습니다.

## endsWith()

```endsWith()``` 메서드는 문자열이 지정된 값으로 끝나면 ```true```를 반환하고, 그렇지 않으면 ```false```를 반환합니다.

###### 예제 12

```javascript
let text = "John Doe";
text.endsWith("Doe");
```

## endsWith() 구문

```javascript
string.endsWith(searchvalue, length)
```

| searchvalue | 필수. 검색할 문자열 |
| length | 선택값. 검색할 길이 |

###### 예제 13

```javascript
let text = "Hello world, welcome to the universe.";
text.endsWith("world", 11);
```

{: .box-note}
```endsWith()``` 메서드는 대소문자를 구분합니다.

## endsWith() 지원 브라우저

```endsWith()```는 ES6 기능(JavaScript 2015)입니다.

모든 최신 브라우저에서 지원됩니다.

```endsWith()```는 Internet Explorer에서 지원되지 않습니다.
