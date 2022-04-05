---
layout: post
title: HTML 43. 멀티미디어 (Multimedia)
subtitle: 웹상의 멀티미디어는 사운드, 음악, 비디오, 영화, 애니메이션입니다.
cover-img: /assets/img/html_img.png
thumbnail-img: /assets/img/html_thumb.png
share-img: /assets/img/html_img.png
tags: [html5, basic]
---

<br>
<a href="https://youtu.be/yC16LS1KsqQ" target="_blank">jiraynor's 하루 2시간 프로그래밍 - HTML 43. 멀티미디어 (Multimedia) 영상 보러가기</a>
<br>
<br>

# HTML 멀티미디어

## 멀티미디어란?

멀티미디어는 다양한 형태로 제공됩니다. 이미지, 음악, 사운드, 비디오, 레코드, 영화, 애니메이션 등 들을 수 있거나 볼 수 있는 거의 모든 것이 될 수 있습니다.

웹 페이지에는 종종 다른 유형과 형식의 멀티미디어 요소가 포함되어 있습니다.

## 지원 브라우저

최초의 웹 브라우저는 텍스트만 지원했으며 단일 색상의 단일 글꼴로 제한되었습니다.

나중에 컬러, 폰트, 이미지, 멀티미디어를 지원하는 브라우저가 등장했습니다!

## 멀티미디어 포멧

멀티미디어 요소(오디오나 비디오 등)는 미디어 파일에 저장됩니다.

파일 형식을 검색하는 가장 일반적인 방법은 파일 확장자를 확인하는 것입니다.

멀티미디어 파일에는 .wav, .mp3, .mp4, .mpg, .wmv 및 .avi와 같은 형식과 확장자가 있습니다.

## 일반적인 비디오 형식

많은 비디오 형식이 있습니다.

MP4, WebM 및 Ogg 형식은 HTML에서 지원됩니다.

MP4 포맷은 유튜브에서 추천합니다.

| 형식 | 확장자 | 설명 |
| MPEG | .mpg .mpeg | MPEG, Moving Pictures Expert Group에 의해 개발되었습니다. 웹에서 가장 인기 있는 비디오 형식입니다. HTML에서는 더 이상 지원되지 않습니다. |
| AVI | .avi | AVI(Audio Video Interleave) Microsoft가 개발. 비디오 카메라 및 TV 하드웨어에 일반적으로 사용됩니다. Windows 컴퓨터에서는 잘 재생되지만 웹 브라우저에서는 잘 재생되지 않습니다. |
| WMV | .wmv | WMV(Windows Media Video). Microsoft가 개발. 비디오 카메라 및 TV 하드웨어에 일반적으로 사용됩니다. Windows 컴퓨터에서는 잘 재생되지만 웹 브라우저에서는 잘 재생되지 않습니다. |
| QuickTime | .mov | Quick Time. Apple이 개발. 비디오 카메라 및 TV 하드웨어에 일반적으로 사용됩니다. Apple 컴퓨터에서는 잘 재생되지만 웹 브라우저에서는 잘 재생되지 않습니다. |
| RealVideo | .rm .ram | RealVideo. 저 대역폭 Real Media를 위해 개발. 웹 브라우저에서는 잘 재생되지 않습니다. |
| Flash | .swf .flv | Flash. Mecromedia에서 개발. 대부분의 경우 웹 브라우저에서 재생하려면 추가 컴포넌트(플러그인)가 필요합니다. |
| Ogg | .ogg | Theora Ogg. Xiph.Org Foundation에서 개발. HTML에서 지원됩니다. |
| WebM | .webm | WebM. Mozilla, Opera, Adobe 및 Google에 의해 개발. HTML에서 지원됩니다. |
| MPEG-4 or MP4 | .mp4 | MP4. Moving Pictures Expert Group에 의해 개발. 비디오 카메라 및 TV 하드웨어에 일반적으로 사용됩니다. 모든 브라우저에서 지원되며 YouTube에서 권장됩니다. |

{: .box-note}
HTML 표준에서는 MP4, WebM 및 Ogg 비디오만 지원됩니다.

## 일반적인 오디오 형식

MP3는 압축된 녹음된 음악에 가장 적합한 형식입니다. MP3라는 용어는 디지털 음악과 동의어가 되었습다.

웹사이트에서 음악을 재생할땐 MP3를 선택할 수 있습니다.

| 형식 | 확장자 | 설명 |
| MIDI | .mid .midi | MIDI(Musical Instrument Digital Interface) 신시사이저나 PC 사운드 카드등의 모든 전자 음악 디바이스의 메인 포맷. MIDI 파일에는 사운드가 포함되어 있지 않지만 전자제품에서 재생할 수 있는 디지털 노트가 포함되어 있습니다. 모든 컴퓨터와 음악 하드웨어에서 잘 재생되지만 웹 브라우저에서는 잘 재생되지 않습니다. |
| RealAudio | .rm .ram | RealAudio. 저대역폭 오디오 스트리밍을 가능하게 하기 위해 Real Media에서 개발. 웹 브라우저에서는 재생되지 않습니다. |
| WMA | .wma | WMA(Windows Media Audio). Microsoft가 개발. Windows 컴퓨터에서는 잘 재생되지만 웹 브라우저에서는 잘 재생되지 않습니다. |
| AAC | .aac | AAC(Advanced Audio Coding). iTunes 기본 포맷으로 Apple에서 개발. Apple 컴퓨터에서는 잘 재생되지만 웹 브라우저에서는 잘 재생되지 않습니다. |
| WAV | .wav | WAV. IBM과 Microsoft가 개발. Windows, Macintosh 및 Linux 운영 체제에서 잘 작동합니다. HTML에서 지원됩니다. |
| Ogg | .ogg | Ogg. Xiph.Org Foundation에서 개발. HTML에서 지원됩니다. |
| MP3 | .mp3 | MP3 파일은 실제로 MPEG 파일의 사운드 부분입니다. MP3는 음악 플레이어들에게 가장 인기 있는 형식이다. 뛰어난 압축성(작은 파일)과 고품질을 겸비합니다. 모든 브라우저에서 지원됩니다. |
| MP4 | .mp4 | MP4는 비디오 형식이지만 오디오에도 사용할 수 있습니다. 모든 브라우저에서 지원됩니다. |

{: .box-note}
HTML 표준에서는 MP3, WAV 및 Ogg 오디오만 지원됩니다.
