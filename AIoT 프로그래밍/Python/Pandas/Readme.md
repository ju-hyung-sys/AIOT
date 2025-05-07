
# 📚 Pandas 기본 개념

Pandas는 Python의 데이터 분석 라이브러리로, 데이터 처리 및 분석을 위한 고성능 데이터 구조를 제공합니다. 주로 `DataFrame`과 `Series`를 사용하여 데이터를 다룹니다.

---

## 1. Pandas 설치

```bash
pip install pandas
```

---

## 2. Pandas import

```python
import pandas as pd
```

---

## 3. 기본 데이터 구조

### 3.1. Series

`Series`는 1차원 배열로, 인덱스와 값으로 구성된 데이터를 표현합니다.

```python
import pandas as pd

s = pd.Series([1, 2, 3, 4])
print(s)
```

출력:
```python
0    1
1    2
2    3
3    4
dtype: int64
```

### 3.2. DataFrame

`DataFrame`은 2차원 데이터 구조로, 표 형식의 데이터를 다룹니다.

```python
data = {'Name': ['Tom', 'Jerry', 'Mickey'], 'Age': [20, 22, 24]}
df = pd.DataFrame(data)
print(df)
```

출력:
```python
     Name  Age
0     Tom   20
1   Jerry   22
2  Mickey   24
```

---

## 4. 기본적인 Pandas 작업

### 4.1. 데이터 파일 읽기

```python
# CSV 파일 읽기
df = pd.read_csv("data.csv")

# Excel 파일 읽기
df = pd.read_excel("data.xlsx")

# JSON 파일 읽기
df = pd.read_json("data.json")
```

### 4.2. 데이터 탐색

```python
df.head()  # 첫 5행을 출력
df.tail()  # 마지막 5행을 출력
df.info()  # 데이터의 정보 (컬럼명, null값 등)
df.describe()  # 수치형 데이터의 통계량 출력
```

### 4.3. 데이터 선택 및 필터링

```python
# 특정 컬럼 선택
df['Name']

# 조건을 만족하는 행 필터링
df[df['Age'] > 21]
```

### 4.4. 데이터 정렬

```python
# Age 컬럼을 기준으로 오름차순 정렬
df.sort_values(by='Age')

# 내림차순 정렬
df.sort_values(by='Age', ascending=False)
```

### 4.5. 데이터 수정

```python
# 새로운 컬럼 추가
df['Score'] = [95, 88, 76]

# 특정 값 변경
df.loc[df['Name'] == 'Tom', 'Age'] = 21
```

---

## 5. 결측치 처리

### 5.1. 결측치 확인

```python
df.isnull()  # 결측값이 있는지 확인
df.isnull().sum()  # 각 컬럼의 결측값 개수 출력
```

### 5.2. 결측치 처리

```python
# 결측값이 있는 행 삭제
df.dropna()

# 결측값을 특정 값으로 채우기
df.fillna(0)
```

---

## 6. 데이터 그룹화

```python
# 'Age'를 기준으로 그룹화하고 평균 계산
df.groupby('Age').mean()
```

---

## 7. 데이터 합치기

### 7.1. 데이터 결합

```python
# 두 DataFrame을 세로로 결합
df1 = pd.DataFrame({'Name': ['Tom', 'Jerry'], 'Age': [20, 22]})
df2 = pd.DataFrame({'Name': ['Mickey'], 'Age': [24]})
df_concat = pd.concat([df1, df2])

# 두 DataFrame을 가로로 결합
df_merge = pd.merge(df1, df2, on='Age')
```

### 7.2. 데이터 분할

```python
# 'Age' 값으로 데이터 분할
df_split = np.array_split(df, 3)
```

---

## 8. 데이터 시각화

```python
import matplotlib.pyplot as plt

# 데이터 시각화
df['Age'].plot(kind='bar')  # 막대그래프
plt.show()
```

---

## 9. 고급 기능

### 9.1. Pivot 테이블

```python
df.pivot_table(values='Score', index='Age', aggfunc='mean')
```

### 9.2. 날짜 처리

```python
df['Date'] = pd.to_datetime(df['Date'])
df['Year'] = df['Date'].dt.year  # 연도만 추출
```

---

## 📝 Pandas 자주 사용하는 함수 요약

| 함수 | 설명 |
|------|------|
| `pd.read_csv()` | CSV 파일 읽기 |
| `df.head()` | 첫 5행 출력 |
| `df.tail()` | 마지막 5행 출력 |
| `df.info()` | 데이터 요약 정보 |
| `df.describe()` | 통계적 요약 |
| `df.isnull()` | 결측값 확인 |
| `df.fillna()` | 결측값 채우기 |
| `df.dropna()` | 결측값 삭제 |
| `df.sort_values()` | 데이터 정렬 |
| `df.groupby()` | 그룹화 및 집계 |
| `pd.to_datetime()` | 날짜 형식 변환 |

---

## 📚 Pandas는 데이터 분석에 매우 유용한 라이브러리로, 데이터 전처리와 통계 분석, 시각화까지 다양한 기능을 제공합니다.

