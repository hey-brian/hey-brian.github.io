---
title: k-Nearest Neighbors
feed: show
date : 2023-04-10
time : 07:21:36
tags : []
format: list
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
- 알고리즘은 데이터(new)가 1개 입력되었을 때, 그 데이터(new)와 가장 가까운 k개의 (known) 데이터가 많이 속하는 label(class)로 그 데이터(new)의 label로 분류(비모수적 확률밀도 추정)

![[/attachments/Pasted_image_20230412072013_watermarked.jpeg]]
- k = 1, 새로운 데이터가 입력되었을 때, 가장 가까운 기존 데이터 1개를 찾고 그 레이블을 그대로 따라간다. (overfitting)
- (\### image by author, code by https://ml-course.github.io)

![[/attachments/Pasted_image_20230412072707_watermarked.jpeg]]
- k = 3, 새로운 데이터가 입력되었을 때, 가장 가까운 기존 데이터 3개를 찾고 그 레이블을 그대로 따라간다. 
- (\### image by author, code by https://ml-course.github.io)

### 1.2 🎓Paper summary
- [[Nearest neighbor pattern classification summary]]
- [[An Important Contribution to Nonparametric Discriminant Analysis and Density Estimation summary_202303270743]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm)

# 2. How It Works
### 2.1 🔑Key 
- KNN은 비모수(non-parametric) 알고리즘으로, 모델을 학습시키지 않고 데이터만을 이용하여 예측을 수행
- KNN은 유사성(similarity) 개념에 기반하여 이웃을 판단한다. 일반적으로 유클리드 거리(Euclidean distance)를 사용하지만, 다른 거리 척도(metric)를 사용할 수도 있다. + 데이터의 스케일링이 중요
- KNN은 k의 값에 따라 예측 결과가 달라진다. 작은 k값은 모델이 노이즈에 민감하게 반응하게 만들 수 있으며, 큰 k값은 모델이 결정 경계(decision boundary)를 보다 부드럽게 만들 수 있다.

![[/attachments/Screenshot_2023-04-10_at_73419_AM_watermarked.jpeg]]

(\### image from [wikipedia](https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm))

# 3. Pros and Cons
- KNN은 과적합(Overfitting) 문제에 강하며, 따라서 상대적으로 적은 데이터셋에서도 좋은 예측 성능을 발휘할 수 있다.
- KNN은 학습 데이터셋의 크기가 커질수록 연산비용이 높아지고 예측 시간이 급격하게 증가하며, 이를 해결하기 위해 효율적인 데이터 구조와 알고리즘을 사용해야 한다. (K-D Tree나 Ball Tree와 같은 효율적인 데이터 구조)
- KNN은 이상치(Outlier)에 민감하기 때문에, 이상치가 있는 경우 이를 처리하는 방법을 고려해야 한다.
- KNN은 차원(dimensionality)이 높아지면 성능이 저하될 가능성이 높다. (curse of dimensionality)
- KNN은 굉장히 직관적이고 구현이 간단하며, 다른 알고리즘과 함께 앙상블(ensemble)로 사용될 수 있다.



_끝_