---
title: Gradient Boosting
feed: show
date : 2023-06-01
tags : [📝️/🌲️, ML]
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
여러 개의 약한 학습기(weak learner)를 순차적으로 학습시켜 강력한 학습기(strong learner)를 만드는 방식으로 동작하는 알고리즘

### 1.2 🎓Paper summary
- [[Greedy function approximation_A gradient boosting machine summary]]
- [[XGBoost_A Scalable Tree Boosting System summary]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Gradient_boosting)

# 2. How It Works
### 2.1 🔑Key 

> 앙상블 학습(ensemble learning)의 한 유형으로, 여러 개의 약한 학습기를 결합하여 강력한 학습기를 구축하는 알고리즘

### 2.2 ⛓️Steps 
1. 초기 모델링: 첫 번째 약한 학습기를 기본 예측값으로 사용한다.
2. 잔차 계산: 초기 예측값과 실제 값 사이의 잔차(오차)를 계산한다.
3. 새로운 모델 학습: 잔차에 대해 다음 약한 학습기를 학습시킨다. 이때, 이전 모델의 예측과 실제 값의 잔차에 초점을 맞추어 학습된다.
4. 예측값 업데이트: 이전 예측값에 새로운 모델의 예측을 더해 업데이트된 예측값을 얻는다.
5. 잔차 업데이트: 이전 잔차에서 새로운 모델의 예측값에 해당하는 잔차를 더해 업데이트한다.
6. 반복: 위 과정을 원하는 개수의 약한 학습기를 반복하여 예측값을 업데이트한다.
7. 최종 예측: 모든 약한 학습기의 예측값을 결합하여 최종 예측값을 얻는다.

![](/attachments/Pasted_image_20230602073127_watermarked.jpeg)

(\=\-\= image from [datascience.eu](https://datascience.eu/machine-learning/gradient-boosting-what-you-need-to-know/))

# 3. Pros and Cons
### 3.1 Pros
- 높은 예측 성능: Gradient Boosting은 약한 학습기를 연속적으로 향상시켜 강력한 모델을 구축해서 예측 성능이 뛰어나다.
- 유연성: 다양한 종류의 데이터와 문제에 적용할 수 있다.
- 변수 중요도 파악: 알고리즘은 변수의 중요도를 추정하여 어떤 변수가 예측에 가장 영향력을 미치는지 파악할 수 있다.

### 3.2 Cons
- 계산 복잡성: 알고리즘은 여러 개의 약한 학습기를 순차적으로 학습하고 결합하기 때문에 계산 비용이 크며, 학습 시간이 오래 걸릴 수 있다.
- 과적합 위험: 모델이 학습 데이터에 과도하게 적합할 수 있으므로, 조정 매개변수나 정규화 기법을 적절히 사용해야 한다.

_끝_