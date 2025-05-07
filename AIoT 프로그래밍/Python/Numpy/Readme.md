
# 📚 Numpy 기본 개념

Numpy는 파이썬에서 과학적 계산을 위한 라이브러리로, 고성능 다차원 배열 객체와 배열을 처리할 수 있는 다양한 함수들을 제공합니다.

---

## 1. Numpy 설치

```bash
pip install numpy
```

---

## 2. Numpy import

```python
import numpy as np
```

---

## 3. 기본 Numpy 객체

### 3.1. Numpy 배열 생성

```python
import numpy as np

# 리스트로 배열 만들기
arr = np.array([1, 2, 3, 4, 5])
print(arr)
```

출력:
```python
[1 2 3 4 5]
```

### 3.2. 다차원 배열

```python
arr_2d = np.array([[1, 2, 3], [4, 5, 6]])
print(arr_2d)
```

출력:
```python
[[1 2 3]
 [4 5 6]]
```

### 3.3. 배열의 차원 확인

```python
arr.ndim  # 배열의 차원
arr_2d.ndim  # 2차원 배열
```

---

## 4. 배열 생성 함수

### 4.1. 0으로 채운 배열

```python
arr_zeros = np.zeros((3, 3))
print(arr_zeros)
```

### 4.2. 1로 채운 배열

```python
arr_ones = np.ones((2, 2))
print(arr_ones)
```

### 4.3. 단위행렬 (Identity matrix)

```python
identity = np.eye(3)
print(identity)
```

### 4.4. 일정 간격으로 배열 생성

```python
arr_range = np.arange(0, 10, 2)
print(arr_range)
```

### 4.5. 지정된 값으로 채운 배열

```python
arr_full = np.full((2, 3), 7)
print(arr_full)
```

---

## 5. 배열 인덱싱과 슬라이싱

### 5.1. 1차원 배열 인덱싱

```python
arr = np.array([1, 2, 3, 4, 5])
print(arr[0])  # 첫 번째 값
```

### 5.2. 2차원 배열 인덱싱

```python
arr_2d = np.array([[1, 2, 3], [4, 5, 6]])
print(arr_2d[0, 1])  # 첫 번째 행, 두 번째 열
```

### 5.3. 배열 슬라이싱

```python
arr = np.array([1, 2, 3, 4, 5])
print(arr[1:4])  # 인덱스 1부터 3까지
```

---

## 6. 배열 연산

### 6.1. 산술 연산

```python
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])

# 덧셈
arr_sum = arr1 + arr2
print(arr_sum)

# 곱셈
arr_mul = arr1 * arr2
print(arr_mul)
```

### 6.2. 브로드캐스팅

```python
arr = np.array([1, 2, 3])
arr2 = arr + 2  # 배열의 각 원소에 2를 더함
print(arr2)
```

### 6.3. 벡터화 연산

```python
arr = np.array([1, 2, 3])
arr_squared = np.square(arr)  # 각 원소의 제곱
print(arr_squared)
```

---

## 7. 배열 통계 함수

```python
arr = np.array([1, 2, 3, 4, 5])

# 합
arr_sum = np.sum(arr)
print(arr_sum)

# 평균
arr_mean = np.mean(arr)
print(arr_mean)

# 표준편차
arr_std = np.std(arr)
print(arr_std)
```

---

## 8. 배열 결합

### 8.1. 수평 결합

```python
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])
arr_combined = np.hstack((arr1, arr2))
print(arr_combined)
```

### 8.2. 수직 결합

```python
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])
arr_combined = np.vstack((arr1, arr2))
print(arr_combined)
```

---

## 9. 배열 변형

### 9.1. 차원 변경 (reshape)

```python
arr = np.array([1, 2, 3, 4, 5, 6])
arr_reshaped = arr.reshape(2, 3)  # 2x3 형태로 변경
print(arr_reshaped)
```

### 9.2. 배열 평탄화 (flatten)

```python
arr_2d = np.array([[1, 2], [3, 4]])
arr_flat = arr_2d.flatten()
print(arr_flat)
```

---

## 📝 Numpy 자주 사용하는 함수 요약

| 함수 | 설명 |
|------|------|
| `np.array()` | 배열 생성 |
| `np.zeros()` | 0으로 채운 배열 |
| `np.ones()` | 1로 채운 배열 |
| `np.arange()` | 일정 간격으로 배열 생성 |
| `np.eye()` | 단위행렬 생성 |
| `np.reshape()` | 배열 차원 변경 |
| `np.sum()` | 합계 계산 |
| `np.mean()` | 평균 계산 |
| `np.std()` | 표준편차 계산 |
| `np.hstack()` | 배열 수평 결합 |
| `np.vstack()` | 배열 수직 결합 |
| `np.flatten()` | 배열 평탄화 |
| `np.full()` | 지정된 값으로 배열 채우기 |
| `np.square()` | 배열 원소의 제곱 |

---

## 📚 Numpy는 과학적 계산을 위한 필수 라이브러리로, 배열 계산, 통계, 선형대수, 푸리에 변환 등 다양한 수학적 연산을 지원합니다.

