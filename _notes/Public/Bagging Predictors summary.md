---
title: Bagging Predictors summary
feed: hide
date : 2022-12-22
time : 08:30:16
tags : [bagging]
format: list
comments: true
---


![](/attachments/Screenshot_2023-03-28_at_105401_PM_watermarked.jpeg)

"Bagging Predictors" 논문은 Breiman에 의해 쓰여진 앙상블 학습에 관한 논문으로, 다수결 방식으로 각각 다른 샘플링 데이터(부트스트랩 방법을 이용하여 표본을 반복 추출)를 이용하여 분류기 학습을 반복하면 일반화 성능을 향상시킬 수 있다는 것을 보여준다. (분산을 줄이고 overfitting을 방지할 수 있음을 실험적으로 입증하였다.) 

# Key Insights and Lessons Learned
- 동일한 알고리즘을 사용하더라도 각 모델은 다른 샘플링 및 부트스트랩 데이터를 사용하여 훈련된다.
- 여러 개의 예측 모델을 결합하면 단일 모델보다 성능이 더욱 향상될 수 있다.
- 결합된 모델의 성능은 모델의 다양성과 정확도에 크게 영향을 받는다.
- Bagging은 일반화 성능을 개선하고 오버피팅을 방지하는데 효과적이다. (예측 오차 감소, 모형 안정성 향상)
- 일반적인 모델의 분산을 줄이는 방법인 배깅(Bagging)의 개념과 각 분류기가 *독립적*으로 학습되는 것이 중요하며(독립적인 예측기 -> 성능 향상), 특히 bootstrap 샘플링 기법을 이용하면 모델 간의 상관성을 낮출 수 있다. 
- 결정트리 분류기를 사용하여 실험하였고, 이를 통해 bagging이 모델의 일반화 성능을 향상시키는 효과를 보여주었다.
- Bagging은 랜덤 포레스트(Random Forest) 알고리즘의 핵심 아이디어이며, 다양한 종류의 예측기에 bagging을 적용할 수 있다.
- Bagging의 주요 목표는 일반화 오류를 줄이는 것이다.

# Related papers
- Hastie, T., Tibshirani, R., & Friedman, J. (2009). The elements of statistical learning: data mining, inference, and prediction. Springer Science & Business Media.
- Zhou, Z. H. (2012). Ensemble methods: foundations and algorithms. CRC press.
- Caruana, R., & Niculescu-Mizil, A. (2006). An empirical comparison of supervised learning algorithms. Proceedings of the 23rd international conference on Machine learning (pp. 161-168).
- Breiman, L. (1996). Bagging predictors. Machine learning, 24(2), 123-140.
- Breiman, L. (1999). Prediction games and arcing algorithms. Neural computation, 11(7), 1493-1517.
- Breiman, L. (2001). Random forests. Machine learning, 45(1), 5-32.
- Dietterich, T. G. (2000). Ensemble methods in machine learning. In Multiple classifier systems (pp. 1-15). Springer, Berlin, Heidelberg.
- Wolpert, D. H. (1992). Stacked generalization. Neural networks, 5(2), 241-259.



_끝_