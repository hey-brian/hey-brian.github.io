---
title: Dropout_A Simple Way to Prevent Neural Networks from Overfitting summary
feed: hide
date : 2023-03-31
time : 23:20:12
tags : [summary]
format: list
comments: true
---

![](/attachments/Screenshot_2023-03-31_at_112144_PM_watermarked.jpeg)

(\### image from [Dropout: A Simple Way to Prevent Neural Networks from Overfitting(2014)](http://jmlr.org/papers/v15/srivastava14a.html))

Dropout이라는 새로운 정규화 기술을 제안하며 이를 사용하여 딥 네트워크의 과적합을 방지하는 방법을 설명한다.

# Key Insights and Lessons Learned
- Dropout은 네트워크의 일부 뉴런을 임의로 선택하여 해당 뉴런의 출력을 0으로 만든다.(무작위로 일부 뉴런을 제거). 이를 통해 각 뉴런의 중요성을 분산시키고(다양한 부분 집합에서 학습 유도) 과적합을 방지할 수 있다.(일반화 성능을 향상).
- Dropout은 모델의 일반화 능력을 향상시키고 다양한 데이터에서 일관된 성능을 보이며, 다른 정규화 기술들과 효과적으로 결합할 수 있다.
- Dropout은 효과적인 regularization 기법이지만, Dropout 확률 값의 선택 및 네트워크 구조와의 상호작용을 고려해야 한다.
- Dropout은 모델 학습 시간이 더 오래 걸릴 수 있지만, 일반화 성능을 향상시켜 모델 성능을 향상시킬 수 있다.

# Related papers
- Goodfellow, I., Bengio, Y., & Courville, A. (2016). Deep learning (Vol. 1). MIT press.
- He, K., Zhang, X., Ren, S., & Sun, J. (2016). Deep residual learning for image recognition. In Proceedings of the IEEE conference on computer vision and pattern recognition (pp. 770-778).
- Kingma, D. P., & Ba, J. (2015). Adam: A method for stochastic optimization. arXiv preprint arXiv:1412.6980.
- LeCun, Y., Bottou, L., Bengio, Y., & Haffner, P. (1998). Gradient-based learning applied to document recognition. Proceedings of the IEEE, 86(11), 2278-2324.
- Zeiler, M. D., & Fergus, R. (2014). Visualizing and understanding convolutional networks. In European conference on computer vision (pp. 818-833).

_끝_