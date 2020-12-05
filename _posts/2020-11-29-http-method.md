---
title: http method
categories: [Springboot]
comments: true
---

#### http method란?
http method는 서버에 요청을 보내는 방법이다.

#### http method의 종류

1. OPTIONS
    - 요청한 URL에 어떠한 메소드 요청이 가능한지 물음
2. GET
    - URL에 해당하는 정보의 전송 요청을 보냄
3. HEAD
    - URL에 해당하는 정보의 전송을 요청하지만, GET과는 다르게 정보의 Meta정보만을 요청
4. POST
    - 서버가 처리할 수 있는 자료를 보낸다. GET으로 보낼 수 없는 자료들에 대해 전송할 때 사용
5. PUT
    - 자료를 전송하여 해당 URL에 자료를 저장
6. DELETE
    - 해당 URL의 자원, 정보를 삭제
7. TRACE
    - 이전까지 요청한 정보들의 목록을 요청
8. CONNECT
    - 프록시가 사용하고 연결을 요청
