# HTTP 프로토콜

웹을 만들기 위해 사용되는 다양한 기술들
* HTTP (HTTPS -> SSL/TLS) -> HTML과 JS와 CSS같은 파일을 웹 서버에게 요청하고 받아오는 프로토콜
---
* HTML ( 웹 페이지를 채울 내용 )
* Javascript ( 웹 페이지에 들어갈 기능 )
* CSS ( 웹 페이지를 예쁘게 꾸밀 디자인 )
>프론트엔트 개발자
---
* ASP/ASP.NET
* JSP
* PHP
>웹 서버 페이지를 만드는 기술들
---
* DB
---
* Python
* Spring
* Jquery
* Ajax
---
## HTTP 프로토콜
HyperText Transfer Protocol ( 하이퍼 텍스트 전송 프로토콜 )
www에서 쓰이는 핵심 프로토콜로 문서의 전송을 위해 쓰이며, 오늘날 거의 모든 웹 애플리케이션에서 사용되고 있다.\
-> 음성, 화상 등 여러 종류의 데이터를 MINE로 정의하여 전송 가능

HTTP 특징\
Request / Response ( 요청/응답 ) 동작에 기반하여 서비스 제공

### HTTP 프로토콜의 특징
HTTP 1.0의 특징
* "연결 수립, 동작, 연결 해제"의 단순함이 특징\
-> 하나의 URL은 하나의 TCP 연결\
HTML 문서를 전송 받은 뒤 연결을 끊고 다시 연결하여 데이터를 전송한다.

HTTP 1.0의 문제점
* 단순 동작 ( 연결 수립, 동작, 연결 해제 )이 반복되어 통신 부하 문제 발생

### HTTP 1.0의 문제점을 보완한 HTTP 1.1
- HTTP 요청 -> HTTP 응답 -> HTTP 요청 -> HTTP 응답 반복 후 연결 종료