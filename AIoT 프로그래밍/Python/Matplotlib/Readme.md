# 📚 Matplotlib 기본 개념

Matplotlib은 Python에서 데이터를 시각화할 수 있는 라이브러리입니다. 특히 2D 그래프를 그리는 데 강력하며, 다양한 유형의 차트를 지원합니다.

---

## 1. Matplotlib 설치

```bash
pip install matplotlib

2. Matplotlib import
import matplotlib.pyplot as plt

3. 기본 그래프
3.1. 선 그래프 (Line Plot)
python
복사
편집
import matplotlib.pyplot as plt

x = [0, 1, 2, 3, 4]
y = [0, 1, 4, 9, 16]

plt.plot(x, y)
plt.title("선 그래프")
plt.xlabel("x 값")
plt.ylabel("y 값")
plt.show()
3.2. 산점도 (Scatter Plot)
python
복사
편집
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [5, 4, 3, 2, 1]

plt.scatter(x, y)
plt.title("산점도")
plt.xlabel("x 값")
plt.ylabel("y 값")
plt.show()
4. 다양한 차트
4.1. 막대 그래프 (Bar Chart)
python
복사
편집
import matplotlib.pyplot as plt

categories = ['A', 'B', 'C', 'D']
values = [10, 20, 15, 30]

plt.bar(categories, values)
plt.title("막대 그래프")
plt.xlabel("카테고리")
plt.ylabel("값")
plt.show()
4.2. 히스토그램 (Histogram)
python
복사
편집
import matplotlib.pyplot as plt

data = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4, 5, 5, 5, 5, 5]

plt.hist(data, bins=5)
plt.title("히스토그램")
plt.xlabel("값")
plt.ylabel("빈도")
plt.show()
4.3. 파이 차트 (Pie Chart)
python
복사
편집
import matplotlib.pyplot as plt

labels = ['A', 'B', 'C', 'D']
sizes = [15, 30, 45, 10]

plt.pie(sizes, labels=labels, autopct='%1.1f%%')
plt.title("파이 차트")
plt.show()
5. 그래프 커스터마이징
5.1. 색상, 스타일, 마커 변경
python
복사
편집
import matplotlib.pyplot as plt

x = [0, 1, 2, 3, 4]
y = [0, 1, 4, 9, 16]

plt.plot(x, y, color='green', linestyle='--', marker='o')
plt.title("커스터마이징된 선 그래프")
plt.xlabel("x 값")
plt.ylabel("y 값")
plt.show()
5.2. 레전드 추가
python
복사
편집
import matplotlib.pyplot as plt

x = [0, 1, 2, 3, 4]
y1 = [0, 1, 4, 9, 16]
y2 = [0, 1, 2, 3, 4]

plt.plot(x, y1, label="y = x^2")
plt.plot(x, y2, label="y = x")
plt.title("두 개의 선 그래프")
plt.xlabel("x 값")
plt.ylabel("y 값")
plt.legend()
plt.show()
6. 서브플롯 (Subplots)
python
복사
편집
import matplotlib.pyplot as plt

x = [0, 1, 2, 3, 4]
y1 = [0, 1, 4, 9, 16]
y2 = [0, 1, 2, 3, 4]

# 1행 2열로 그래프 생성
plt.subplot(1, 2, 1)
plt.plot(x, y1)
plt.title("y = x^2")

plt.subplot(1, 2, 2)
plt.plot(x, y2)
plt.title("y = x")

plt.tight_layout()  # 그래프 간 간격을 자동으로 맞춤
plt.show()
7. 그래프 저장
python
복사
편집
import matplotlib.pyplot as plt

x = [0, 1, 2, 3, 4]
y = [0, 1, 4, 9, 16]

plt.plot(x, y)
plt.title("선 그래프")
plt.xlabel("x 값")
plt.ylabel("y 값")

# 그래프를 이미지로 저장
plt.savefig("line_plot.png")
plt.show()
8. 고급 기능
8.1. X, Y 축 설정
python
복사
편집
import matplotlib.pyplot as plt

x = [0, 1, 2, 3, 4]
y = [0, 1, 4, 9, 16]

plt.plot(x, y)
plt.xlim(-1, 5)  # x축 범위 설정
plt.ylim(-1, 20)  # y축 범위 설정
plt.title("축 범위 설정")
plt.show()
8.2. 그리드 추가
python
복사
편집
import matplotlib.pyplot as plt

x = [0, 1, 2, 3, 4]
y = [0, 1, 4, 9, 16]

plt.plot(x, y)
plt.grid(True)  # 그리드 추가
plt.title("그리드가 있는 선 그래프")
plt.show()
📝 Matplotlib 자주 사용하는 함수 요약
함수	설명
plt.plot()	선 그래프 그리기
plt.scatter()	산점도 그리기
plt.bar()	막대 그래프 그리기
plt.hist()	히스토그램 그리기
plt.pie()	파이 차트 그리기
plt.title()	그래프 제목 설정
plt.xlabel(), plt.ylabel()	x, y 축 레이블 설정
plt.legend()	범례 추가
plt.subplot()	서브플롯 생성
plt.tight_layout()	서브플롯 간 간격 자동 조정
plt.savefig()	그래프를 파일로 저장
plt.grid()	그리드 추가

📚 Matplotlib은 데이터 시각화에서 매우 유용한 도구로, 다양한 유형의 차트를 손쉽게 그릴 수 있습니다.
