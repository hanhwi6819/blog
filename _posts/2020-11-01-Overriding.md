---
title: Overriding
categories: [JAVA]
comments: true
---

#### 메소드 오버라이딩(method overriding)
**: 상속받은 부모 클래스의 메소드를 재정의하여 사용하는 것**
- 자바에서 자식 클래스는 부모 클래스의 private 멤버를 제외한 모든 메소드를 상속받음
- 그대로 사용 또는 재정의하여 사용 가능

---

#### 오버라이딩의 조건
- 메소드의 선언부는 기존 메소드와 완전히 같아야 한다. (반환 타입은 부모 클래스의 반환 타입으로 변환할 수 있으면 변경 가능)
- 부모 클래스의 메소드보다 접근 제어자를 더 좁은 범위로 변경할 수 없다.
- 부모 클래스의 메소드보다 더 큰 범위의 예외를 선언할 수 없다.
 
 ---

**예제**
```java
class Parent {
    void display() { System.outprintln("부모 클래스의 display() 메소드입니다."); }
}
class Child extends Parent {
    void display() { System.outprintln("자식 클래스의 display() 메소드입니다."); }
}
 
public class Inheritance05 {
    public static void main(String[] args) {
        Parent pa = new Parent();
        pa.display();
        Child ch = new Child();
        ch.display();
        Parent pc = new Child();
        pc.display(); // Child cp = new Parent();
    }
}

```

**출력값**
```
부모 클래스의 display() 메소드입니다.
자식 클래스의 display() 메소드입니다.
자식 클래스의 display() 메소드입니다.
```