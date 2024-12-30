### 클래스란 무엇인가?
-----
```python
class 클래스이름:
    def __init__(self, 매개변수):
        self.속성 = 매개변수  # 속성 초기화

    def 메서드(self):
        print("메서드 호출")
```

예를들어
```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

    def display_info(self):
        print(f"자동차 브랜드: {self.brand}, 모델: {self.model}")

# 객체 생성
car1 = Car("Tesla", "Model S")
car1.display_info()

결과
자동차 브랜드: Tesla, 모델: Model S
```

키오스크로 생각하기
```python
class MenuItem:
    def __init__(self, name, price, description):
        self.name = name
        self.price = price
        self.description = description

    def __str__(self):
        return f"선택하신 음식은 {self.name}이고, {self.price}이며 - {self.description}한 음식입니다."

menuA = MenuItem("a", "1000원", "aaa")
menuB = MenuItem("b", "2000원", "bbb")
menuC = MenuItem("c", "3000원", "ccc")

menuA.__str__()

결과 
선택하신 음식은 a이고, 1000원이며 - aaa한 음식입니다.
```
생산자 메서드(32~36) = 키오스크 기본 틀

메서드(38~39) = 문장틀

객체(인스턴스)(41~43) = 버튼

45 = A음식 버튼

결과 = A음식에 대한 주문 페이지








```python
class NewList():
    def init_list(self, 1):
        self.list = 1

a = NewList()
a.init_list(1, 2)
```
#def init_list(self, 1): 에서 'self'와 '1' 두개가 있으니깐 a.init_list(1, 2)에 '1'과 '2' 두개를 대입함 (self=1, 1=2)

#그러면 self.list = 1에서 에러가 생김(1.list = 2) 2개의 인자를 받아야하는데 3개의 인자를 받음.

#함수와 메서드의 동작 방식때문

#함수는 선언때 입력하는 인자 개수와 실행때 입력하는 입력 개수가 서로 대응

#메서드에선 a.init_list(1, 2)에 인스턴스(점앞에 a)를 집어넣음

#그러므로 a.init_list(1, 2)가 아니라         a.init_list(2)가 맞는표현
