---
title: Stochastic Gradient Descent
feed: show
date : 2023-05-25
tags : [📝️/🌲️, ML]
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
- Stochastic Gradient Descent(SGD)는 경사하강법([[Gradient Descent]])의 변형으로, 대규모 데이터셋에서 모델을 효율적으로 학습한다. SGD는 미니 배치라고 불리는 작은 샘플 그룹을 사용하여 각 반복에서 모델 파라미터를 업데이트한다.

### 1.2 🎓Paper summary
- [[A Stochastic Approximation Method summary]]
- [[Stochastic Estimation of the Maximum of a Regression Function summary]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Stochastic_gradient_descent)

# 2. How It Works
### 2.1 🔑Key 

> 모든 학습 데이터를 한 번에 사용하지 않고, 미니 배치를 사용하여 파라미터를 업데이트해서 `계산 효율성을 높이는 것` 이다. 이를 통해 대규모 데이터셋에서도 모델을 효과적으로 학습가능하다.

### 2.2 ⛓️Steps 
1. 초기에는 모델의 파라미터를 무작위로 설정한다. (weight initialization)
2. 학습 데이터셋에서 미니 배치를 선택한다.
3. 선택된 미니 배치에 대해 손실 함수를 계산하고, 현재 모델 파라미터에 대한 기울기를 구한다.
4. 구한 기울기를 사용하여 모델 파라미터를 업데이트한다. 이때, 학습률(learning rate)이라 불리는 하이퍼파라미터를 사용하여 업데이트의 크기를 조절한다. (weight update)
5. 2~4단계를 반복하여 모든 미니 배치에 대해 모델 파라미터를 업데이트한다.
6. 반복을 통해 파라미터가 조정되며, 모델의 손실을 최소화한다.
7. 모든 학습 데이터에 대해 반복적인 업데이트를 수행한 후, 최종적으로 학습된 모델을 얻는다.

![](/attachments/Pasted_image_20230526071339_watermarked.jpeg)

(\### image from [medium](https://sweta-nit.medium.com/batch-mini-batch-and-stochastic-gradient-descent-e9bc4cacd461))

![](/attachments/Pasted_image_20230526071235_watermarked.jpeg)

(\### image from [medium](https://sweta-nit.medium.com/batch-mini-batch-and-stochastic-gradient-descent-e9bc4cacd461))

# 3. Pros and Cons
### 3.1 Pros
- 대규모 데이터셋에서도 효율적인 학습이 가능하다.
- 계산량이 적으므로 빠른 학습이 가능하다.
- 다양한 모델에 적용할 수 있다.

### 3.2 Cons
- SGD는 잡음이 많은 데이터에서 최적화 과정이 불안정할 수 있다.
- 학습률이 잘 설정되어야 하며, 너무 작거나 큰 값은 학습 결과에 영향을 줄 수 있다.

_끝_