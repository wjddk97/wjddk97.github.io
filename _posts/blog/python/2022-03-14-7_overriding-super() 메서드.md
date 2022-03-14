---
layout: post
title: 7. overriding/ super() 메서드
#subtitle: 부제목
tags: 
# description: >
#   설명
related_posts:
categories:
   - blog
   - python
---

* toc
{:toc .large-only}

## Overriding 오버라이딩

---

- <u>오버라이딩은 부모 클래스의 메서드를 자식 클래스에 재정의 하여 사용하는 것을 의미한다.</u>

<br>

```python
class Parent:
    def over(self):
        print(f'부모 클래스의 over 메서드입니다.')

class Child(Parent):
    def over(self):
        print(f'자식 클래스의 over 메서드입니다.')

ex = Child()
ex.over()

-----
자식 클래스의 over 메서드입니다.
```

<br>


## super()

---

- <u>자식 클래스에서 부모클래스의 내용을 사용하고 싶은 경우</u> **super()** 이용

<br>

**예시 1**

```python
class Parent:
    def over(self):
        print(f'부모 클래스의 over 메서드입니다.')

class Child(Parent):
    def over(self):
        super().over() #부모클래스의 over 메서드 호출
        print(f'자식 클래스의 over 메서드입니다.')

ex = Child()
ex.over()

-----
부모 클래스의 over 메서드입니다.
자식 클래스의 over 메서드입니다.
```

<br>

**예시 2**

```python
class Animal():
    def __init__( self, name ):
        self.name = name

class Human(Animal):
    def __init__( self, name, phone ):
        super().__init__( name ) # 부모클래스의 __init__ 메서드 호출
        self.phone = phone

person = Human( "김모모", "010-1111-1111" )
print(person.name)
print(person.phone)

-----
김모모
010-1111-1111
```