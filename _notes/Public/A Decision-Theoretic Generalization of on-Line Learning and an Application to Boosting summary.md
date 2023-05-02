---
title: A Decision-Theoretic Generalization of on-Line Learning and an Application to Boosting summary
feed: hide
date : 2023-03-28
time : 07:40:31
tags : [summary]
format: list
comments: true
---


![](/attachments/Screenshot_2023-03-28_at_104832_PM_watermarked.jpeg)

(\### image from  [A Decision-Theoretic Generalization of on-Line Learning and an Application to Boosting](https://link.springer.com/chapter/10.1007/3-540-59119-2_166))

Freund와 Schapire의 "A Decision-Theoretic Generalization of on-Line Learning and an Application to Boosting" 논문은 지수 손실 함수를 최적화하여 약한 학습자들을 결합하여 강한 학습자를 형성하는 AdaBoost라는 온라인 학습용 알고리즘 프레임워크를 제안.

# Key Insights and Lessons Learned
- AdaBoost는 간단한 약한 학습자를 사용하여 분류 작업의 정확도를 크게 개선할 수 있는 강력하고 견고한 알고리즘이다.
- 지수 손실 함수는 다른 손실 함수보다 오분류에 민감하며, 오분류된 샘플에 초점을 맞추는 데 사용될 수 있다.
- 이 논문은 Boosting 알고리즘의 수학적 기반과 이론적 배경을 분석하였으며, 이를 바탕으로 Boosting 알고리즘의 성능을 향상시키기 위한 방법을 제안. (AdaBoost 성능의 이론적 보장)
	- 약한 학습자가 일정한 조건을 만족한다면 항상 학습 오류가 0인 분류기로 수렴
- AdaBoost는 얼굴 감지, 물체 인식, 스팸 필터링 등 많은 실제 응용 분야에서 사용

# Related papers
- Freund, Y., & Schapire, R. E. (1997). A decision-theoretic generalization of on-line learning and an application to boosting. Journal of computer and system sciences, 55(1), 119-139.
- Friedman, J. H. (2001). Greedy function approximation: a gradient boosting machine. Annals of statistics, 29(5), 1189-1232.
- Hastie, T., Tibshirani, R., & Friedman, J. (2009). The elements of statistical learning: data mining, inference, and prediction. Springer Science & Business Media.
- Schapire, R. E. (1990). The strength of weak learnability. Machine learning, 5(2), 197-227.
- Breiman, L. (1996). Bagging predictors. Machine learning, 24(2), 123-140.

_끝_