---
title: getter & setter
categories: [JAVA]
comments: true
---

### getter / setter
클래스의 특성 중 정보 은닉(Hiding information)을 가장 잘 보여주는 메소드
private로 접근제한한 멤버 변수의 값을 변경, 호출한다.

**※접근제어자(access modifier)**
정보 은닉을 구체화하기 위한 도구
1. private
2. public
3. default
4. protected


```java

public class Phone {
    // 멤버 변수
    private int price;
    private String company;
    private int display;
    private int weight;
    private int grade;
    private String kind;

    // 생성자 메소드
    public Phone(int price, String company) {
        this.price = price;
        this.company = company;
    }

    // setter
    public void setPrice(int price) {
        this.price = price;
    }

    public void setCompany(String company) {
        this.company = company;
    }
    // getter
    public int getPrice() {
        return price;
    }

    public String getCompany() {
        return company;
    }
```