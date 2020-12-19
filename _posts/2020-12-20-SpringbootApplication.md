---
title: SpringbootApplication
categories: [Springboot]
comments: true
---

SpringbootApplication
===

```java

@RestController
@AllArgsConstructor 
public class TestController {

    private TestService testService;

    // /api/test로 요청이 오면 문자열 HelloWorld 반환
    @GetMapping(value = "/api/test")
    public String helloWorld() {
        return "HelloWorld";
    }

    // /api/user로 요청이 오면 testService.getUserList를 반환
    @GetMapping(value = "/api/user")
    public List<User> getUserList() { // 원래는 List 타입이다.
        return testService.getUserList();
    }

    // /api/user{userId}로 요청이 오면 testService.getUser(userId)를 반환
    @GetMapping(value = "/api/user/{userId}")
    public Optional<User> getUser(@PathVariable Long userId) {
        return testService.getUser(userId);
    }
}

```

① @RestController
- 컨트롤러를 JSON을 반환하는 컨트롤러로 만들어 준다.
- 예전에는 @ResponseBody를 각 메소드마다 선언했던 것을 한번에 사용할 수 있게 해준다고 생각하면 된다.

② @AllArgsConstructor
- 클래스에 존재하는 모든 필드에 대한 생성자를 자동으로 생성해줍니다.

③ @GetMapping
- HTTP Method인 Get의 요청을 받을 수 있는 API를 만들어 준다.
(예전에는 @RequestMapping(method = RequestMethod.GET)으로 사용되었다.)
