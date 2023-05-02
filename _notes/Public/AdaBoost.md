---
title: AdaBoost
feed: show
date : 2023-04-01
tags : [📝️/🌲️, ML]
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
- 아다부스트(AdaBoost), 즉 적응형 부스팅([[Boosting]]): 이진 분류 문제의 정확도를 향상시키는 머신러닝 알고리즘으로 약한 분류기들을 결합하여 강한 분류기 학습.

### 1.2 🎓Paper summary
- [[A Decision-Theoretic Generalization of on-Line Learning and an Application to Boosting summary]]
- [[Experiments with a New Boosting Algorithm summary]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/AdaBoost)

# 2. How It Works
### 2.1 🔑Key 
> 최종 예측은 `약한 분류기 예측의 가중합`으로 구성되며, 정확한 분류기에 더 높은 가중치가 부여

### 2.2 ⛓️Steps 
- 아다부스트는 학습 데이터의 서로 다른 하위 집합에서 반복적으로 약한 분류기(weak classifier)를 학습하고, 이들의 예측을 결합하여 최종 예측 수행. 
- 각 약한 분류기는 정확도에 따라 가중치를 받으며, 이전 분류기에 의해 잘못 분류된 샘플에는 이후 반복에서 더 높은 가중치가 부여되며 학습 진행.

# 3. Pros and Cons
### 3.1 😄Pros
- AdaBoost는 다양한 분류 문제에 적용 가능
- 상대적으로 쉽게 구현할 수 있으며, 전반적으로 효과적인 알고리즘
- 노이즈가 있는 데이터와 이상치를 처리하는데도 활용 가능
- 대용량 데이터셋을 처리할 수 있는 빠른 속도

### 3.2 😅Cons
- 약한 분류기가 너무 복잡하거나 이상치가 심한 데이터일 경우 영향을 받음 (일반적인 알고리즘 특성..)
- 약한 분류기 개수가 너무 많거나 약한 분류기가 너무 느리면 (약한 분류기가 조합되는 알고리즘이기에) 계산 비용이 크게 증가할 수 있음
- 약한 분류기가 너무 복잡하거나 데이터셋이 작을 경우 과적합 가능성 존재
- 성능을 개선하기 위해서는 매개변수를 조정 필요 (일반적인 알고리즘 특성..)


_끝_