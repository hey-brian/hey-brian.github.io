---
title: Elastic Net
feed: show
date : 2023-06-01
tags : [📝️/🌲️, ML]
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
- Elastic Net은 회귀 분석에서 사용되는 정규화 기법으로, L1 규제와 L2 규제를 조합하여 모델의 복잡도를 조절하고 변수를 선택

### 1.2 🎓Paper summary
- [[Regularization and variable selection via the Elastic Net summary]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Elastic_net_regularization)
- [Elastic Net talk by Hui Zou and Trevor Hastie](https://hastie.su.domains/TALKS/enet_talk.pdf)

# 2. How It Works
### 2.1 🔑Key 

> L1 규제와 L2 규제를 조합한 정규화 기법

![](/attachments/Pasted_image_20230610232041_watermarked.jpeg)

(\### image from [Elastic Net talk by Hui Zou and Trevor Hastie](https://hastie.su.domains/TALKS/enet_talk.pdf))

### 2.2 ⛓️Steps 

![](/attachments/Pasted_image_20230607081458_watermarked.jpeg)

(\### image by author)

1. L1 규제와 L2 규제의 가중치를 결정하기 위해 혼합 비율(alpha) 값을 선택한다.
2. 초기 회귀 모델을 설정하고, 경사 하강법이나 좌표 하강법과 같은 최적화 알고리즘을 사용하여 가중치를 업데이트한다.
3. 업데이트된 가중치를 기반으로 잔차를 계산하고, 잔차의 크기에 따라 변수의 중요도를 판단한다.
4. 중요도가 낮은 변수는 제외하고, 중요도가 높은 변수는 유지하며 모델을 다시 업데이트한다.
5. 위의 과정을 반복하여 최적의 가중치와 변수 선택을 찾는다.

# 3. Pros and Cons
### 3.1 Pros
- 변수 선택과 모델의 복잡도 조절을 동시에 수행할 수 있다.
- Lasso 회귀의 한계인 변수 선택의 불안정성을 완화시킨다.
- 다중공선성 문제를 효과적으로 다룰 수 있다.
- Elastic Net은 상관 관계가 강한 변수들을 함께 선택하는 경향이 있어, 모델의 편향을 줄이고 예측 성능을 향상시킬 수 있다.

### 3.2 Cons
- 혼합 비율(alpha) 값을 선택하는 것이 중요하며, 이 값에 따라 모델의 성능이 달라질 수 있다.
- Elastic Net은 변수의 갯수가 많은 경우에도 잘 작동하지만, 변수의 갯수가 적을 때에는 Lasso나 Ridge와 같은 단일 규제 방법이 더 선호될 수 있다.
- 모델 해석력이 Lasso보다는 떨어질 수 있다.

# 4. Application
- 예측 모델링
	- 변수 선택과 모델 복잡도 조절이 필요한 경우에 Elastic Net을 사용하여 예측 모델을 구축할 수 있다.
- 유전 연구
	- 유전자 선택 및 관련 특성들의 연관성 분석에 Elastic Net이 널리 사용된다.
- 이미지 처리
	- 이미지 분류, 세그멘테이션 등에서 특징 선택을 위해 Elastic Net이 활용된다.
- 금융 분야
	- 주가 예측, 포트폴리오 최적화 등에서 변수 선택과 정규화에 Elastic Net을 활용할 수 있다.
- 생물정보학
	- 유전자 표현 데이터 분석, 단백질 구조 예측 등에 Elastic Net이 적용된다.

_끝_