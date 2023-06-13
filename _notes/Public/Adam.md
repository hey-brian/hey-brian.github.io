---
title: Adam
feed: show
date : 2023-06-13
time : 07:38:03
tags : []
format: list
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
- Adam (Adaptive Moment Estimation) 최적화는 딥 러닝에서 널리 사용되는 최적화 알고리즘이며, 학습 속도를 자동으로 조절하고 모멘텀을 효과적으로 관리하는 기능을 제공한다.

### 1.2 🎓Paper summary
- [[Adam_A Method for Stochastic Optimization summary]]

### 1.3 🔗Useful links
- [Cornell](https://optimization.cbe.cornell.edu/index.php?title=Adam)

# 2. How It Works
### 2.1 🔑Key 
> 모멘텀과 학습률을 자동으로 조절하여 수렴속도를 향상

### 2.2 ⛓️Steps 
1. 초기화: 학습률(learning rate)과 모멘텀 계수(beta1, beta2)를 설정하고, 파라미터의 초기 값을 지정한다.
2. Gradient 계산: 모델의 손실 함수를 기반으로 파라미터에 대한 gradient를 계산한다.
3. 모멘텀 적용: 이전 스텝에서 계산된 모멘텀을 사용하여 파라미터 업데이트를 진행한다.
4. Bias 보정: 초기 학습 단계에서 모멘텀이 부족한 문제를 완화하기 위해, 일부 bias 보정을 수행한다.
5. 모멘텀 및 학습률 조정: 계산된 gradient를 이용하여 모멘텀과 학습률을 조절한다.
6. 파라미터 업데이트: 새로운 학습률과 모멘텀을 사용하여 파라미터 값을 업데이트한다.
7. 반복: 위의 단계를 반복하여 최적의 파라미터를 찾는다.

![](/attachments/Pasted_image_20230613074502_watermarked.jpeg)

(\### image from [Cornell](https://optimization.cbe.cornell.edu/index.php?title=Adam))

# 3. Pros and Cons
### 3.1 😄Pros
- 학습률을 자동으로 조절하여 수렴 속도를 향상시킨다.
- 많은 하이퍼파라미터 튜닝이 필요하지 않고, 기본 설정값이 대부분의 경우 잘 작동한다.
- 모멘텀을 적절하게 관리하여 지역 최소값에 빠지지 않고 전역 최소값을 찾는데 도움을 준다.
- 경사 하강법보다 효율적으로 파라미터를 업데이트하여 빠른 학습을 도모한다.

### 3.2 😅Cons
- 일부 문제에서는 다른 최적화 알고리즘보다 성능이 떨어질 수 있다.
- 메모리 사용량이 높을 수 있으며, 모델 크기가 큰 경우에는 학습 속도가 저하될 수 있다.
- 모든 파라미터에 대해 일괄적인 학습률이 적용되기 때문에, 특정 파라미터에 대한 학습을 잘못 조절할 수 있다.

_끝_