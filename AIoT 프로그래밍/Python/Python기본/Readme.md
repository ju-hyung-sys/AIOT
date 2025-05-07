
# 🐍 파이썬(Python) 기본 문법 정리

## 1. 🖐️ 출력  
```python  
print("Hello, World!")  
```

## 2. 📦 변수와 자료형  
```python  
name = "Alice"     # 문자열  
age = 25           # 정수  
height = 160.5     # 실수  
is_student = True  # 불리언  
```

## 3. 🔢 연산자  

| 종류 | 예시 | 설명 |
|------|------|------|
| 산술 | `+`, `-`, `*`, `/`, `//`, `%`, `**` | 더하기, 빼기, 곱하기, 나누기, 몫, 나머지, 제곱 |
| 비교 | `==`, `!=`, `<`, `>`, `<=`, `>=` | 같음, 다름, 크기 비교 |
| 논리 | `and`, `or`, `not` | 논리 연산 |

## 4. 🔀 조건문  
```python  
if age >= 20:  
    print("성인입니다.")  
elif age >= 13:  
    print("청소년입니다.")  
else:  
    print("어린이입니다.")  
```

## 5. 🔁 반복문  

### for문  
```python  
for i in range(5):  
    print(i)  
```

### while문  
```python  
i = 0  
while i < 5:  
    print(i)  
    i += 1  
```

## 6. 📦 리스트(List)  
```python  
fruits = ["apple", "banana", "cherry"]  
print(fruits[0])      # 'apple'  
fruits.append("kiwi") # 리스트에 추가  
```

## 7. 📦 딕셔너리(Dictionary)  
```python  
person = {"name": "Tom", "age": 20}  
print(person["name"])  
person["age"] = 21  
```

## 8. 🎯 함수(Function)  
```python  
def greet(name):  
    return f"Hello, {name}!"  
  
print(greet("Alice"))  
```

## 9. 🐞 예외 처리 (try-except)  
```python  
try:  
    num = int(input("숫자 입력: "))  
    print(10 / num)  
except ZeroDivisionError:  
    print("0으로 나눌 수 없습니다!")  
except ValueError:  
    print("숫자를 입력하세요!")  
```

## ✅ 자주 쓰는 내장 함수  

| 함수 | 설명 |
|------|------|
| `len()` | 길이 |
| `type()` | 자료형 확인 |
| `int()`, `str()`, `float()` | 형 변환 |
| `range()` | 범위 생성 |
| `input()` | 사용자 입력 받기 |

## 📌 보너스: 리스트 컴프리헨션  
```python  
squares = [x**2 for x in range(5)]  # [0, 1, 4, 9, 16]  
```

---

🧠 파이썬은 문법이 간단해서 배우기 쉬워요!  
💪 예제를 많이 따라 해보면 금방 익숙해지고, 실력도 훨씬 빨리 늘어요!

