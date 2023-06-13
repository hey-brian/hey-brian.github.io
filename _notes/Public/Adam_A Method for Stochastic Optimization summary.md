---
title: Adam_A Method for Stochastic Optimization summary
feed: hide
date : 2023-03-29
time : 07:26:34
tags : [summary]
format: list
comments: true
---

![](/attachments/Screenshot_2023-03-29_at_73122_AM_watermarked.jpeg)

(\### image from [Adam: A Method for Stochastic Optimization(2015)](https://arxiv.org/abs/1412.6980))

Kingma와 Ba의 "Stochastic Optimization을 위한 Adam 방법" 논문은 기존의 최적화 알고리즘인 Momentum과 Adagrad를 개선하여 더 빠르고 효과적인 학습이 가능한 Adam 알고리즘을 제안한다.

# Key Insights and Lessons Learned
- Adam 알고리즘은 Momentum과 Adagrad의 장점을 결합하여 최적화 알고리즘의 성능을 대폭 개선시킨다.
- Adam은 모멘텀 최적화와 RMSProp의 장점을 결합한 알고리즘으로, 다양한 문제에서 우수한 성능을 보인다.
- Adam 알고리즘은 자동으로 학습률을 조절하며, 이를 통해 다양한 하이퍼파라미터 튜닝을 줄이고 성능을 개선할 수 있다.
- Adam 알고리즘은 불규칙한 그레이디언트를 처리하는 데 효과적이다.
- Adam은 하이퍼파라미터를 튜닝하기 쉽고, 일반적인 하이퍼파라미터 값이 다른 최적화 알고리즘과 비교하여 성능이 우수하다.
- Adam은 불규칙한 그래디언트에 강하며, 볼록 함수와 비볼록 함수 모두에서 잘 동작한다.

# Related papers
- Duchi, J., Hazan, E., & Singer, Y. (2011). Adaptive subgradient methods for online learning and stochastic optimization. Journal of machine learning research, 12(Jul), 2121-2159.
- Zeiler, M. D. (2012). ADADELTA: an adaptive learning rate method. arXiv preprint arXiv:1212.5701.
- Ruder, S. (2016). An overview of gradient descent optimization algorithms. arXiv preprint arXiv:1609.04747.
- Bottou, L. (2010). Large-scale machine learning with stochastic gradient descent. In Proceedings of COMPSTAT'2010 (pp. 177-186). Physica-Verlag HD.

_끝_