---
title: Random Forest
feed: show
date : 2023-05-04
tags : [📝️/🌲️, ML]
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
- Random Forest(랜덤 포레스트)는 의사결정나무(Decision Tree)를 활용하여 생성하는 앙상블(Ensemble) 기반 머신러닝 모델

### 1.2 🎓Paper summary
- [[Random Forests summary]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Random_forest)

# 2. How It Works
### 2.1 🔑Key 

> 많은 수의 결정 트리를 생성하고 출력을 결합하는 기계 학습 알고리즘

### 2.2 ⛓️Steps 
- 분류, 회귀 및 기타 작업을 위한 앙상블 학습 방법으로 많은 수의 결정 트리를 구성하며 데이터를 학습한다.
- 새로운 데이터에 대해서는 **개별 트리의 클래스 최빈값**(분류 문제) 또는 **예측값의 평균**(회귀 문제)으로 예측 수행한다.

![](/attachments/Pasted_image_20230504074503_watermarked.jpeg)

(\### image from [Wikipedia](https://en.wikipedia.org/wiki/Random_forest))

# 3. Pros and Cons
### 3.1 Pros
- 다양한 데이터 유형과 문제에 적용 가능하며, 좋은 예측 결과를 보여준다.
- 특정 피처가 다른 모델보다 중요도를 더 부여받아 해석 가능한 결과를 도출할 수 있다.
- 피처의 스케일링과 정규화가 필요하지 않으며, 누락 데이터 처리가 간단하다.
- 모델 학습 과정에서 다양한 부트스트랩 샘플과 랜덤 피처 추출로 인한 다양성을 제공하여 과적합을 방지한다.

### 3.2 Cons
- 모델 해석력이 낮아 결과를 설명하기 어려울 수 있다.
- 대규모 데이터셋의 경우 학습 시간이 오래 걸릴 수 있다.
- 일부 경우 딥러닝 등의 다른 모델보다 성능이 떨어질 수 있다.

# 4. Related articles
- Breiman, L. (2001). Random forests. Machine Learning, 45(1), 5-32.
- Liaw, A., & Wiener, M. (2002). Classification and regression by random forest. R news, 2(3), 18-22.
- Cutler, D. R., Edwards Jr, T. C., Beard, K. H., Cutler, A., Hess, K. T., Gibson, J., & Lawler, J. J. (2007). Random forests for classification in ecology. Ecology, 88(11), 2783-2792.
- Chen, T., & Guestrin, C. (2016). Xgboost: A scalable tree boosting system. In Proceedings of the 22nd acm sigkdd international conference on knowledge discovery and data mining (pp. 785-794).
- Biau, G., & Scornet, E. (2016). A random forest guided tour. Test, 25(2), 197-227.


_끝_