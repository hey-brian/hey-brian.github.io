---
title: Learning representations by back-propagating errors summary
feed: hide
date : 2023-03-31
time : 23:04:28
tags : [summary]
format: list
comments: true
---

![](/attachments/Screenshot_2023-03-31_at_110601_PM_watermarked.jpeg)

(\### image from [Learning representations by back-propagating errors(1986)](https://www.nature.com/articles/323533a0))

역전파 알고리즘을 사용하여 인공신경망에서 입력과 출력 사이의 연결 가중치를 학습하는 방법을 통해 인공신경망의 학습 효율성을 증가시키는 방법은 제시했다.

# Key Insights and Lessons Learned
- 역전파 알고리즘은 인공신경망에서 효과적인 학습 방법으로, 입력과 출력 사이의 연결 가중치를 조정하여 원하는 출력을 만드는 방법을 학습한다.
- 중간층의 활성화 함수는 비선형 함수여야 한다.
- 가중치 초기화, 활성화 함수의 종류, 학습 속도(rate) 등의 하이퍼파라미터를 조정하는 것이 학습 성능에 큰 영향을 미친다.
- 오버피팅을 방지하기 위해 가중치 감소, 조기 종료 등의 방법을 사용할 수 있다.
- 역전파 알고리즘을 사용하여 다층 신경망이 선형 분류 문제와 비선형 분류 문제를 모두 해결할 수 있다는 것을 실험적으로 입증했다.

# Related papers
- LeCun, Y., Bengio, Y., & Hinton, G. (2015). Deep learning. Nature, 521(7553), 436-444.
- He, K., Zhang, X., Ren, S., & Sun, J. (2016). Deep residual learning for image recognition. In Proceedings of the IEEE conference on computer vision and pattern recognition (pp. 770-778).
- Glorot, X., & Bengio, Y. (2010). Understanding the difficulty of training deep feedforward neural networks. In Proceedings of the thirteenth international conference on artificial intelligence and statistics (pp. 249-256).
- Kingma, D. P., & Ba, J. (2014). Adam: A method for stochastic optimization. arXiv preprint arXiv:1412.6980.
- Goodfellow, I., Bengio, Y., & Courville, A. (2016). Deep learning (Vol. 1). MIT press.



_끝_
