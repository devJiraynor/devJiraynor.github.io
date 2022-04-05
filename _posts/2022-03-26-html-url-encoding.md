---
layout: post
title: HTML 33. URL 인코딩 (URL Encoding)
subtitle: URL은 웹 주소의 다른 단어입니다. URL은 단어 또는 인터넷 프로토콜(IP) 주소로 구성할 수 있습니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<a href="https://youtu.be/G9MhXx4eW-k" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 33. URL 인코딩 (URL Encoding) 영상 보러가기</a>
<br>
<br>

# HTML URL(Uniform Resource Locators)

## URL - Uniform Resource Locators

웹 브라우저는 URL을 사용하여 웹 서버에 페이지를 요청합니다.

URL(Uniform Resource Locator)은 웹상의 문서(또는 기타 데이터)를 수신처로 지정하기 위해 사용됩니다.

웹 주소는 다음 구문 규칙을 따릅니다.

##### scheme://prefix.domain:port/path/filename

###### 설명

+ scheme - 인터넷서비스 유형을 정의합니다(가장 일반적인 것은 http 또는 https).
+ prefix - 도메인프리픽스를 정의합니다(http 기본값은 www).
+ domain - 인터넷 도메인 이름(github.com 등)을 정의합니다.
+ port - 호스트의 포트 번호를 정의합니다(http 기본값은 80).
+ path - 서버의 경로를 정의합니다( 생략할 경우 사이트의 루트 디렉토리).
+ filename - 문서 또는 리소스의 이름을 정의합니다.

## 일반적인 URL 방식

다음 표에 일반적인 방식을 몇 가지 나타냅니다.

| scheme | 줄임말 | 사용처 |
| http | HyperText Transfer Protocol | 일반적인 웹 페이지. 암호화되어 있지 않습니다. |
| https | Secure HyperText Transfer Protocol | 안전한 웹 페이지. 암호화되어 있습니다. |
| ftp | File Transfer Protocol | 파일 다운로드 또는 업로드 |
| file |  | 컴퓨터에 있는 파일 |

## URL 인코딩

URL, ASCII 문자셋을 사용해 인터넷을 개입시켜 송신할 수 있습니다. URL에 ASCII 이외의 문자가 포함되어 있는 경우는, URL을 변환할 필요가 있습니다.

URL 인코딩은 non-ASCII 문자를 인터넷을 통해 전송할 수 있는 형식으로 변환합니다.

URL 인코딩은 non-ASCII 문자를 "%"와 16진수 뒤에 이어지는 문자로 바꿉니다.

URL에는 공백을 포함할 수 없습니다. URL 인코딩은 보통 공간을 플러스 기호(+) 또는 %20으로 바꿉니다.

## 시도해보기

<form action="https://www.w3schools.com/action_page2.php" method="GET">
  <input type="text" value="안녕하세요." name="text" size="30" />
  <input type="submit" value="Submit" />
</form>

**Submit**을 클릭하면 브라우저는 입력이 서버로 전송되기 전에 URL을 인코딩합니다.

서버의 페이지에 수신한 입력이 표시됩니다.

다른 입력을 시도하고 **Submit**(제출)을 다시 클릭합니다.

## ASCII 인코딩 예시

브라우저는 페이지에서 사용되는 문자 집합에 따라 입력을 인코딩합니다.

HTML5 의 디폴트 문자 세트는 UTF-8 입니다.

| 문자 | window-1252 | utf-8 |
| € | %80 | %E2%82%AC |
| £ | %A3 | %C2%A3 |
| © | %A9 | %C2%A9 |
| ® | %AE | %C2%AE |
| À | %C0 | %C2%80 |
| Á | %C1 | %C2%81 |
| Â | %C2 | %C2%82 |
| Ã | %C3 | %C2%83 |
| Ä | %C4 | %C2%84 |
| Å | %C5 | %C2%85 |
