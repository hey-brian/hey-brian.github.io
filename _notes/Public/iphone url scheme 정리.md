---
title: iphone url scheme 정리
feed: show
date : 2022-12-14
time : 23:18:17
tags : []
comments: true
---

## iphone url scheme 목록 정리
- shortcut 등을 작성할 때 사용할 수 있는 아이폰앱 URL scheme을 정리했다. (지속 업데이트 예정)
- {내용} 은 \{, \} 를 제외하고 **내용**에 해당하는 문자를 입력한다.  
	- ex) https://{웹사이트 주소} -> https://hey-brian.github.io

| 제목                    | 기능                      | URL scheme                                                   | 비고    |
| ----------------------- | ------------------------- | ------------------------------------------------------------ | ------- |
| spotify                 | 가수노래 재생             | spotify://spotify:artist:{가수ID}                            | spotify |
| spotify                 | 앨범 재생                 | spotify://spotify:album:{앨범ID}                             | spotify |
| spotify                 | 열기                      | spotify://                                                   | spotify |
| wallet                  | 열기                      | shoebox://                                                   | apple   |
| youtube music(Youtube)  | 열기                      | youtube://                                                   | youtube |
| youtube music(YT music) | 목록 재생                 | youtubemusic://watch?list={재생목록링크}                     | youtube |
| youtube music(YT music) | 열기                      | youtubemusic://                                              | youtube |
| 계산기                  | 열기                      | calc://                                                      | apple   |
| 구글 캘린더             | 열기                      | com.google.calendar://?action=view&type=event                | google  |
| 구글 캘린더             | 열기                      | com.google.calendar://                                       | google  |
| 구글 캘린더             | 일정 추가                 | com.google.calendar://?action=create                         | google  |
| 굿노트5                 | 열기                      | goodnotes5://                                                | app     |
| 네이버 TV               | 열기                      | naverplayer://                                               | naver   |
| 네이버 메일             | 열기                      | navermail://                                                 | naver   |
| 네이버 밴드             | 열기                      | bandapp://                                                   | naver   |
| 네이버 블로그           | 열기                      | naverbolg://                                                 | naver   |
| 네이버 지도             | 열기                      | navermap://                                                  | naver   |
| 네이버 카페             | 열기                      | navercafe://                                                 | naver   |
| 네이버 캘린더           | 열기                      | navercal://                                                  | naver   |
| 네이버 클라우드(MYBOX)  | 열기                      | ndrive://                                                    | naver   |
| 넷플릭스                | 열기                      | nflx://                                                      | netflix |
| 단축어(shortcut)        | 갤러리 열기               | shortcuts://gallery                                          | apple   |
| 단축어(shortcut)        | 단축어 설치               | shortcuts://shortcuts/{ShortcutID}                           | apple   |
| 단축어(shortcut)        | 단축어 실행               | shortcuts://run-shortcut?name={shortcut이름}                 | apple   |
| 단축어(shortcut)        | 단축어 앱 열기            | shortcuts://                                                 | apple   |
| 단축어(shortcut)        | 단축어 열기               | shortcuts://open-shortcut?name={shortcut이름}                | apple   |
| 단축어(shortcut)        | 새로운 단축어             | shortcuts://create-shortcut                                  | apple   |
| 단축어(shortcut)        | 클립보드 포함 단축어 실행 | shortcuts://run-shortcut?name={shortcut이름}&input=clipboard | apple   |
| 메모                    | 열기                      | mobilenotes://                                               | apple   |
| 메시지                  | 새로운 텍스트             | sms://                                                       | apple   |
| 메시지                  | 수신인 지정하여 새 메시지 | sms-private://TheirPhoneNumber                               | apple   |
| 메시지                  | 수신인 지정하여 새 메시지 | sms://TheirPhoneNumber                                       | apple   |
| 메시지                  | 열기                      | messages://                                                  | apple   |
| 메일                    | 메일 보내기               | mailto:{메일주소}                                            | apple   |
| 메일                    | 열기                      | message://                                                   | apple   |
| 멜론                    | 열기                      | fb329785880437397://                                         | kakao   |
| 미리알림                | 열기                      | x-apple-reminder://                                          | apple   |
| 미리알림                | 열기                      | x-apple-reminderkit://                                       | apple   |
| 사진                    | 열기                      | photos-redirect://                                           | apple   |
| 사파리                  | FTP 파일 열기             | ftp://{ftp서버의 파일경로}                                    | apple   |
| 사파리                  | FTP 파일 열기             | x-web-search://{파일경로}                                    | apple   |
| 사파리                  | HTTP 사이트 열기          | http://{웹사이트 주소}                                       | apple   |
| 사파리                  | HTTPS 사이트 열기         | https://{웹사이트 주소}                                      | apple   |
| 사파리                  | 열기                      | http://{원하는 사이트 주소}                                  | apple   |
| 사파리                  | 열기                      | x-web-search://                                              | apple   |
| 설정                    | 열기                      | App-prefs://                                                 | apple   |
| 시계                    | 세계시계                  | clock-worldclock://                                          | apple   |
| 시계                    | 수면알람                  | clock-sleep-alarm://                                         | apple   |
| 시계                    | 스톱워치                  | clock-stopwatch://                                           | apple   |
| 시계                    | 알람                      | clock-alarm://                                               | apple   |
| 시계                    | 타이머                    | clock-timer://                                               | apple   |
| 앱스토어                | 열기                      | itms-apps://itunes.apple.com                                 | apple   |
| 연락처                  | 열기                      | contact://                                                   | apple   |
| 전화                    | 보이스메일                | vmshow://                                                    | apple   |
| 전화                    | 열기                      | mobilephone://                                               | apple   |
| 전화                    | 전화 바로 걸기            | tel://TheirPhoneNumber                                       | apple   |
| 전화                    | 전화 바로 걸기            | telprompt://TheirPhoneNumber                                 | apple   |
| 전화                    | 즐겨찾기                  | mobilephone-favorites://                                     | apple   |
| 전화                    | 최근 통화                 | mobilephone-recents://                                       | apple   |
| 주식                    | 열기                      | stocks://                                                    | apple   |
| 지도                    | 열기                      | map://                                                       | apple   |
| 카카오 T                | 열기                      | kakaot://                                                    | kakao   |
| 카카오 T                | 택시 호출                 | kakaot://taxi?dest_lat={위도}&dest_lng={경도}                | kakao   |
| 카카오페이              | 열기                      | kakaopay://                                                  | kakao   |
| 캘린더                  | 열기                      | calshow://                                                   | apple   |
| 파일                    | 열기                      | shareddocuments://                                           | apple   |
| 페이스타임              | 영상전화시작              | facetime-prompt://{핸드폰 번호 또는 이메일}                  | apple   |
| 페이스타임              | 영상전화시작              | facetime://{핸드폰 번호 또는 이메일}                         | apple   |
| 페이스타임              | 음성전화시작              | facetime-audio-prompt://{핸드폰 번호 또는 이메일}            | apple   |
| 페이스타임              | 음성전화시작              | facetime-audio://{핸드폰 번호 또는 이메일}                   | apple   |
| 구글메일                | 열기                      | googlegmail://                                               | google  |
| 구글메일                | 열기                      | googlegmail://                                               | google  |
| 구글캘린더              | 열기                      | googlecalendar://                                            | google  |
| 구글독스                | 열기                      | googledocs://                                                | google  |
| 구글크롬                | 열기                      | googlechrome://                                              | google  |
| 구글드라이브            | 열기                      | googledrive://                                               | google  |
| 구글킵                  | 열기                      | comgooglekeep://                                             | google  |
| 구글지도                | 열기                      | googlemaps://                                                | google  |
| 구글사진                | 열기                      | googlephotos://                                              | google  |
| 구글시트                | 열기                      | googlesheets://                                              | google  |
| 인스타그램              | 열기                      | instagram://                                                 | instagram    |
| 페이스북 메신져         | 열기                      | fb-messenger://                                              | facebook    |
| 트위치                  | 열기                      | twitch://                                                    | twitch  |
| 트위터                  | 열기                      | twitter://                                                   | twitter |
| 페이스북 메신져         | 열기                      | fb-messenger://                                              | meta    |

## 출처:
- [Complete List of iOS URL Schemes for Apple Apps and Services (Always-Updated)](https://medium.com/@contact.jmeyers/complete-list-of-ios-url-schemes-for-apple-apps-and-services-always-updated-800c64f450f)
- [Always-Updated List of iOS App URL Scheme](https://www.phoneweek.co.uk/always-updated-list-of-ios-app-url-scheme-names-ios-iphone-gadget-hacks/)
