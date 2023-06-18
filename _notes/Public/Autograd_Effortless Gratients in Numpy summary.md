---
title: Autograd_Effortless Gratients in Numpy summary
feed: hide
date : 2023-03-31
time : 07:48:42
tags : []
format: list
comments: true
---

![](/attachments/Screenshot_2023-03-31_at_74912_AM_watermarked.jpeg)

(\### image from [Autograd: Effortless Gratients in Numpy(2015)](https://indico.ijclab.in2p3.fr/event/2914/contributions/6483/subcontributions/180/attachments/6060/7185/automl-short.pdf)

"Autograd_Effortless Gradients in Numpy" 논문은 Dougal Maclaurin, David Duvenaud, Ryan P. Adams가 저술한 논문으로, Numpy 기반으로 자동 미분을 수행하는 Autograd를 제시하여 딥러닝 모델 학습에서 기울기(미분) 계산을 보다 쉽게 처리할 수 있도록 하였다.

# Key Insights and Lessons Learned
- Autograd는 Python 기반의 라이브러리로 일반적인 연산을 수행하는 Numpy 함수를 자동 미분 가능한 형태로 변환하여, **딥러닝 모델 학습에서 기울기 계산을 자동으로 처리**할 수 있는 기능을 제공한다.
- Autograd는 머신러닝 모델 학습 및 최적화 과정에서 그래디언트 계산을 효율적으로 수행할 수 있는 기술을 제공하며, 다른 머신러닝 프레임워크와 연계하여 사용될 수 있다. (오버헤드를 최소화하면서도 효율적으로 그래디언트를 계산)
- Autograd는 **미분의 연쇄 법칙(chain rule)을 이용하여 다양한 연산에 대한 그래디언트를 계산**할 수 있으며, 코드 구현이 단순하고 직관적이다.
- Autograd는 간단하고 직관적인 API를 제공하며, 딥러닝 모델 학습에서 중요한 역할을 하는 역전파(backpropagation) 알고리즘을 자동으로 생성해주는 장점이 있다.
- Autograd를 통해 개발된 딥러닝 모델은 일반적인 Numpy 배열과 같이 사용할 수 있기 때문에, 기존의 코드를 그대로 활용할 수 있는 장점이 있다.

# Related papers
- Baydin, A. G., Pearlmutter, B. A., Radul, A. A., & Siskind, J. M. (2018). Automatic differentiation in machine learning: a survey. Journal of Machine Learning Research, 18(1), 5595-5637.
- Maclaurin, D., Duvenaud, D., & Adams, R. P. (2015). Gradient-based hyperparameter optimization through reversible learning. In Proceedings of the 32nd International Conference on Machine Learning (ICML-15) (pp. 2113-2122).
- Paszke, A., Gross, S., Massa, F., Lerer, A., Bradbury, J., Chanan, G., ... & Chintala, S. (2019). PyTorch: An imperative style, high-performance deep learning library. In Advances in Neural Information Processing Systems (pp. 8024-8035).
- Jax Development Team. (2021). Jax: composable transformations of Python+NumPy programs.
- Chen, T., & Duvenaud, D. (2018). Neural network optimization: Analytical bounds, graph connectivity and neural architecture search. arXiv preprint arXiv:1807.04872.

_끝_
