---
title: Bagging
feed: show
date : 2023-04-14
time : 07:34:13
tags : []
format: list
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
Bagging은 Bootstrap Aggregating의 줄임말로, 각각의 [[Bootstrap]](중복을 허용) sample(데이터)들을 모아서 (Aggregating) 여러 개의 모델을 만들고 예측하는 앙상블 방법

### 1.2 🎓Paper summary
- [[Bagging Predictors summary]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Bootstrap_aggregating)

# 2. How It Works
### 2.1 🔑Key 

> `여러 개의 부트스트랩 샘플(bootstrap sample)`을 사용하여 더 안정적이고 정확한 예측 모델을 만드는 통계 기법

### 2.2 ⛓️Steps 
- 학습 데이터의 여러 무작위(bootstrap) 샘플을 만들고, 각 샘플마다 별도의 예측 모델을 학습한 후, 이러한 모델들의 예측을 결합하여 최종 예측

![](/attachments/Pasted_image_20230426074440_watermarked.png)

(\### image from [Wikipedia](https://en.wikipedia.org/wiki/Bootstrap_aggregating))


# 3. Pros and Cons
### 3.1 Pros
- Bagging은 다양한 모델을 만들어 **편향-분산 트레이드오프를 개선**할 수 있다.
- 데이터를 무작위로 선택(Bootstrap 샘플링)하고 학습하기 때문에 **오버피팅(overfitting) 방지**할 수 있다.
- Bagging은 분류와 회귀 문제 모두에서 효과적으로 작동한다.
- 높은 분산을 가지는 모델에 적용할 경우 더 큰 성능 향상을 기대할 수 있다.
- 앙상블 모델로 다양한 모델을 결합해줌으로써 **예측 성능을 높인다**.
- Outlier에 대한 강건성 (Robustness)을 제공합니다.
- 병렬 처리가 가능하여 계산 시간을 단축시켜줍니다.

### 3.2 Cons
- 데이터의 서로 다른 하위 집합에서 여러 모델을 학습하기 때문에 **계산 비용이 크다**.
- 여러 모델을 사용하면 **모델이 복잡해지기** 때문에(complexity) 결과를 해석/설명하기 힘들어진다.
- Bagging에 사용되는 각각의 모델이 이미 정확한 경우, Bagging 결과가 만족스럽지 않을 수 있다. (정확도 향상 측면)
- 모델의 분산을 줄일 수 있지만, 각각의 모델이 서로 너무 유사한 경우 편향을 증가시킬 수 있습니다.
- 데이터셋 크기, 모델의 개수, 부트스트랩 샘플링 비율 등의 하이퍼파라미터를 조정하는 것이 중요

# 4. Application
- 의사결정나무(decision trees), 랜덤 포레스트(random forests), 서포트 벡터 머신(support vector machines) 등 다양한 머신러닝 알고리즘에 적용될 수 있다.

_끝_