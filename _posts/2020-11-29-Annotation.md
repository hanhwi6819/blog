---
title: Annotation
categories: [Springboot]
comments: true
---

# _Annotation_

#### Annotation(@)의 의미

코드 사이에 주석처럼 쓰여서 특별한 의미, 기능을 수행하도록 하는 기술이다. 즉, 프로그램에게 추가적인 정보를 제공해주는 메타데이터(meta data : 데이터를 위한 데이터)라고 볼 수 있다.

---

#### Annotation 용도

- 컴파일러에게 코드 작성 문법 에러를 체크하도록 정보를 제공

- 소프트웨어 개발 툴이 빌드나 배치시 코드를 자동으로 생성할 수 있도록 정보 제공

- 실행시(런타임시) 특정 기능을 실행하도록 정보를 제공

---

#### Annotation 순서

1. Annotation의 정의
2. 클래스에 배치
3. 코드 실행중에 Reflection을 이용하여 추가정보를 획득 ▶ 기능 실시

---

#### Annotation 종류

어노테이션 | 설명 | 사용
---|:---:|---:
`@Controller` | 스프링 MVC의 컨트롤러 객체임을 명시하는 어노테이션 | 클래스
`@RequestMapping` | 특정 URI에 미챙되는 클래스나 메소드임을 명시하는 어노테이션  | 클래스, 메소드
`@RequestParam` | 요청에서 특정한 파라미터 값을 찾아낼 때 사용하는 어노테이션 | 파라미터
`@RequestHeader` | 요청에서 특정 HTTP헤더 정보를 추출할 때 | 파라미터
`@PathVariable` | 현재의 URI에서 원하는 정보를 추출할 때 사용하는 어노테이션 | 파라미터
`@CookieValue` | 현재 사용자의 쿠키가 존재하는 경우 쿠키의 이름을 이용해서 쿠키의 값을 추출 | 파라미터
`@ModelAttribute` | 자동으로 해당 객체를 뷰까지 전달하도록 만드는 어노테이션 | 메소드, 파라미터
`@InitBinder` | 파라미터를 수집해서 객체로 만들 경우에 커스터마이징 | 메소드
`@ResponseBody` | 리턴 타입이 HTTP의 응답 메시지로 전송 | 메소드, 리턴타입
`@RequestBody` | 요청 문자열이 그대로 파라미터로 전달 | 파라미터
`@Repository` | DAO 객체 | 클래스
`@Service` | 서비스 객체 | 클래스
`@SessionAttribute` | 세션상에서 모델의 정보를 유지하고 싶은 경우에 사용 | 클래스