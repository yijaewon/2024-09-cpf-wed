# 2024-09-cpf-wed
2024 가을 프로그래밍 기초 수요일반 Colab 실습

*1주차 Hello World 실습

| 주차 | 실습 |
|:-----:|:-----:|
| 1 | Hello World |
| 2 | Github Classrooms |
| 3 | github Action |

import numpy as np
import matplotlib.pyplot as plt

# x, y 값의 그리드 생성
x = np.linspace(-3, 3, 400)
y = np.linspace(-3, 3, 400)
X, Y = np.meshgrid(x, y)

# 함수 f(x, y) = x^2 - y^2 계산
Z = X**2 - Y**2

# 등고선 그리기
plt.contour(X, Y, Z, levels=np.arange(-3, 4, 1), cmap='coolwarm')
plt.xlabel('x')
plt.ylabel('y')
plt.title(r'함수 $f(x, y) = x^2 - y^2$의 등고선')
plt.colorbar(label='f(x, y)')
plt.grid(True)
plt.show()
