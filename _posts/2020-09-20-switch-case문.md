---
title: switch case문
categories: [JAVA]
comments: true
---

#### switch case문

```java
switch (menuNumber) {
	case 1: // 조건의 값이 1일때 실행
	    System.out.println("빅맥 세트입니다.");
	    break;
	case 2:
	    System.out.println("치즈 세트입니다.");
		break;
    case 3:
		System.out.println("맥너겟 세트입니다.");
		break;

	default: // 조건이 나머지일때 실행
		System.out.println("안녕하세요 맥도날드입니다.");
		break;
}
```