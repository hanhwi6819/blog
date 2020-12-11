---
title: Controller
categories: [Springboot]
comments: true
---

#### Spring Boot - Controller

**controller란?**

- 사용자의 요청이 진입하는 지점(entry point)

- 요청에 따라 어떤 처리를 할지 결정

단, controller는 단지 결정만 해주고 실질적인 처리는 서비스(Layered Architecture)에서 담당

- 사용자에게 View(또는 서버에서 처리된 데이터를 포함하는 View)를 응답으로 보냄

----

**controller를 사용하는 이유**

요청에 따라 로직처리를 위한 분기를 담당하고 사용자에게 서버에서 처리된 데이터를 포함한 View를 리턴한다.

_역할분담이 핵심이다._

----

**사용 예시**

```java
@Controller
@RequestMapping("/questions")
public class QuestionController {
    @PostMapping()
        public String create(@LoginUser User loginUser, QuestionDto questionDto) {
            qnaService.create(loginUser, questionDto);
            return "redirect:/";
        }
    @PutMapping("/{id}")
    public String update(@LoginUser User loginedUser, @PathVariable Long id, QuestionDto questionDto) {
        ...
    }

    @DeleteMapping("/{id}")
    public String delete(@LoginUser User logindUser, @PathVariable Long id) {
        ...
    }
}
```

- QuestionController는 `/questions`로 시작하는 path에 반응
1. 사용자가 회원가입을 할 때 개인정보를 입력하고 `회원가입`버튼을 누르면
2. `http://localhost:8080/questions` 요청
3. controller는 이를 인식하여 create() 호출
4. create()는 리턴 값으로 `redirect:/` 리턴