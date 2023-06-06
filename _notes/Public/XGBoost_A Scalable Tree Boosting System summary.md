---
title: XGBoost_A Scalable Tree Boosting System summary
feed: hide
date : 2023-03-29
time : 07:08:53
tags : [summary]
format: list
comments: true
---

![](/attachments/Screenshot_2023-03-29_at_70833_AM_watermarked.jpeg)

(\### image from [XGBoost: A Scalable Tree Boosting System(2016)](https://arxiv.org/abs/1603.02754))

이 논문은 트리 부스팅 알고리즘의 성능을 향상시키기 위해 그래디언트 부스팅 프레임워크의 일반화를 제안하고, 분산 처리 및 고효율성을 갖는(대규모 데이터셋에 대해 높은 예측 성능을 제공) XGBoost 알고리즘을 소개한다. 그리고 분산환경에서의 XGBoost의 효율적인 구현 방법과 함께 성능 향상 기법에 대해 설명한다. (feat. 정규화, 과적합 방지)

# Key Insights and Lessons Learned
- 유연한 파라미터 조정 기능을 제공한다.
- Regularization 기법과 조기 종료 기능이 과적합을 방지하고, 모델의 일반화 성능을 향상시킨다.
- 분산 처리를 지원하며, 대규모 데이터셋에서 효율적으로 동작한다.
- 분산환경에서의 확장성과 효율성을 높이기 위한 멀티쓰레딩, 분산 학습 및 압축 기능 등의 구현 방법이 있다.
- 가중치 부여 및 이상치 처리와 같은 기능이 데이터 전처리에 대한 수고를 줄일 수 있다.

# Related papers
- Friedman, J. H. (2001). Greedy function approximation: A gradient boosting machine. Annals of statistics, 29(5), 1189-1232.
- Chen, T., & Guestrin, C. (2016). XGBoost: A scalable machine learning system. In Proceedings of the 22nd ACM SIGKDD International Conference on Knowledge Discovery and Data Mining (pp. 785-794).
- Ke, G., Meng, Q., Finley, T., Wang, T., Chen, W., Ma, W., ... & Liu, T. Y. (2017). LightGBM: A highly efficient gradient boosting decision tree. In Advances in Neural Information Processing Systems (pp. 3146-3154).
- Chen, T., & He, T. (2018). XGBoost: Reliable large-scale tree boosting system. In Proceedings of the 26th ACM International Conference on Information and Knowledge Management (pp. 1-4).
- Chen, T., & Guestrin, C. (2016). XGBoost: A Scalable Tree Boosting System. arXiv preprint arXiv:1603.02754.

_끝_