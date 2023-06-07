---
title: Lasso
feed: show
date : 2023-06-01
tags : [📝️/🌲️, ML]
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
- Lasso (Least Absolute Shrinkage and Selection Operator)는 회귀 문제에서 변수 선택과 모델 특성 선택을 위한 알고리즘.

### 1.2 🎓Paper summary
- [[Linear Inversion of Band-Limited Reflection Seismograms summary]]
- [[Regression Shrinkage and Selection Via the Lasso summary]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Lasso_(statistics)%EC%9D%98)

# 2. How It Works
### 2.1 🔑Key 

> Lasso는 L1 규제를 사용하여 모델의 가중치를 축소하는 방식으로 작동하며, 이를 통해 Lasso는 중요한 변수를 선택하고 불필요한 변수의 영향을 줄인다.

### 2.2 ⛓️Steps 

![](/attachments/Pasted_image_20230607081458_watermarked.jpeg)

(\### image by author)

1. 선형 회귀 모델에 L1 규제를 적용하는 방식으로 작동한다. (가중치 값을 제한하여 모델을 단순화)
2. Lasso는 최적화 문제로 정의되며, 목표는 잔차 제곱합과 L1 규제 항의 합을 최소화하는 가중치를 찾는다.
3. 경사 하강법이나 좌표하강법과 같은 최적화 알고리즘을 사용하여 가중치를 업데이트한다. 이 때, L1 규제 항은 가중치의 크기에 따라 미분 가능하지 않으므로 부분 미분값을 사용하여 가중치를 업데이트한다.
4. Lasso 알고리즘은 가중치 값을 0으로 축소시키는 특성을 가진다. 이를 통해 중요하지 않은 변수의 가중치를 0으로 만들어 변수 선택을 수행하고, 모델의 복잡성을 줄인다.
5. Lasso는 규제 파라미터인 알파(alpha) 값을 조정하여 가중치 축소의 강도를 조절한다. (작은 알파 값은 가중치 축소를 강화하고, 큰 알파 값은 가중치 축소를 약화)

# 3. Pros and Cons
### 3.1 Pros
- 변수 선택: Lasso는 변수 선택 기능을 제공하여 중요한 변수를 식별하고 모델의 복잡성을 줄일 수 있습니다.
- 해석 가능성: Lasso는 모델의 가중치를 축소하므로 결과를 해석하기 쉽습니다.
- 다중공선성 처리: Lasso는 다중공선성 문제를 해결하는 데 도움을 줄 수 있습니다.

### 3.2 Cons
- 모델 복잡성 제한: Lasso는 모델의 가중치를 제한하므로 복잡한 모델에 적합하지 않을 수 있습니다.
- 변수 선택의 한계: Lasso는 선택한 변수 외에는 정보를 제공하지 않으며, 모든 변수가 중요하지 않을 수 있습니다.
- 변수 상관 관계 처리: Lasso는 변수 간의 상관 관계를 고려하지 않으므로 상관 관계가 있는 변수를 제대로 처리하지 못할 수 있습니다.

# 4. Application
- 특성 선택 (Feature Selection)
	- Lasso는 관련 없거나 중요성이 낮은 특성의 계수를 제로로 축소하여 특성 선택을 수행하는 데 사용된다. 이를 통해 예측 모델 구축을 위한 가장 관련성 있는 특성을 식별하고 모델의 해석 가능성을 향상시킨다.
- 회귀 분석 (Regression Analysis)
	- Lasso는 회귀 분석에서 널리 사용되며, 특히 고차원 데이터셋을 다룰 때 유용하다. 예측 변수의 개수가 관측값의 개수보다 많은 경우에도 적합하게 처리하여 다중공선성(multicollinearity) 문제를 해결하고 모델 성능을 향상시킨다.
- 신호 처리 (Signal Processing)
	- Lasso는 잡음 제거 및 신호 복원과 같은 신호 처리 작업에서 활용됩니다. 계수 추정에서 희소성을 촉진함으로써, Lasso는 신호에서 잡음을 효과적으로 제거하고 누락된 또는 손상된 데이터를 복원할 수 있습니다.
- 생물 정보학 (Bioinformatics)
	- Lasso는 유전자 선택과 생물학적 마커 식별에 사용된다. 특정 생물학적 결과 또는 질병 상태를 예측하는 데 가장 관련성 있는 유전자 또는 유전자 마커의 하위 집합을 식별하는 데 유용하다.
- 이미지 처리 (Image Processing)
	- Lasso는 이미지 노이즈 제거, 채우기 및 압축 센싱과 같은 이미지 처리 작업에 적용된다. 희소성을 촉진하여 이미지에서 노이즈를 제거하고 누락된 픽셀을 채우며, 표현에서 희소성을 유지함으로써(promoting sparsity in the representation) 이미지를 압축할 수 있다.

_끝_
