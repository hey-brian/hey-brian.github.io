---
title: Greedy function approximation_A gradient boosting machine summary
feed: hide
date : 2023-03-28
time : 07:48:58
tags : [summary]
format: list
comments: true
---

![](/attachments/Screenshot_2023-03-28_at_105448_PM_watermarked.jpeg)

(\### image from [Greedy function approximation: A gradient boosting machine(2001)](https://projecteuclid.org/euclid.aos/1013203451))

이 논문은 모델 내에서 다른 모델들의 가중 조합을 사용하는 boosting 알고리즘의 변형인 Gradient Boosting Machine(GBM)를 제안하고, 주어진 문제를 해결하기 위해 부스팅을 사용할 때 유용한 일반적인 프레임워크를 제공한다.

# Key Insights and Lessons Learned
- 변수 선택 및 변수 중요도 분석에 유용하다.
- 함수 근사 문제를 그리디한 방식으로 접근하여 반복적으로 새로운 함수를 추가하면서 손실을 최소화하는 방법을 제안하였다. 
- GBM 알고리즘이 다른 모델보다 높은 예측 성능을 보이며, 특히 일부 예측 변수 간에 강한 상호작용이 있는 경우에 유용하다는 것을 실험적으로 입증하였다. 
- 오버피팅을 방지하기 위한 규제 기법을 포함할 수 있다.
- 데이터의 특성에 따라 다양한 하이퍼파라미터 조합을 실험하여 모델의 성능을 극대화할 수 있음을 밝혔다.
- 다양한 종류의 예측 모델과 결합할 수 있으며, 일반적으로 결합된 모델의 성능이 더 좋아진다.
- 과적합과 같은 일반적인 기계 학습 문제를 다루는 데 유용하다.

# Related papers
- Chen and Guestrin, (2016). "XGBoost: A Scalable Tree Boosting System" 
- Ke et al., (2017). "LightGBM: A Highly Efficient Gradient Boosting Decision Tree"
- Prokhorenkova et al., (2018). "CatBoost: unbiased boosting with categorical features" 
- Lopez-Paz and Ranzato, (2017). "Deep Learning using Linear Support Vector Machines" 
- He et al., (2021). "AutoML: A Survey of the State-of-the-Art" 

_끝_