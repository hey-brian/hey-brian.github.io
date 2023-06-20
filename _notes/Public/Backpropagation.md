---
title: Backpropagation
feed: show
date : 2023-06-20
time : 07:37:03
tags : []
format: list
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
- 역전파(Back-propagation)는 신경망의 학습 알고리즘으로, 입력 데이터를 통해 손실 함수에 대한 그래디언트를 효율적으로 계산하여 가중치(weights)와 편향(bias)을 업데이트하는 기능을 제공한다.

### 1.2 🎓Paper summary
- [[Learning representations by back-propagating errors summary]]
- [[Backpropagation Applied to Handwritten Zip Code Recognition summary]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Backpropagation)


# 2. How It Works
### 2.1 🔑Key 
> 입력 데이터의 손실 함수(loss function)에 대한 그래디언트(gradient)를 효율적으로 계산하여 손실을 줄이는 방향으로 가중치(weights)와 편향(bias)을 업데이트

### 2.2 ⛓️Steps 
1. 초기화: 가중치와 편향을 임의의 값으로 초기화한다.
2. 전진 패스: 입력 데이터를 신경망에 전달하여 각 뉴런의 출력값을 계산한다.
3. 손실 함수 계산: 실제 값과 예측 값 간의 오차를 측정하기 위해 손실 함수를 계산한다.
4. 역전파: 손실 함수의 그래디언트를 계산하기 위해 역전파 알고리즘을 사용한다.
5. 그래디언트 업데이트: 역전파로 얻은 그래디언트를 사용하여 가중치와 편향을 업데이트한다.
6. 반복: 위의 단계를 반복하여 손실을 최소화하고 모델을 훈련시킨다.

![](/attachments/Pasted_image_20230621071916_watermarked.jpeg)

(\### image from [Adam](https://stackoverflow.com/users/2082623/adam)'s [Stackoverflow](https://stackoverflow.com/questions/22054877/backpropagation-training-stuck))

# 3. Pros and Cons
### 3.1 😄Pros
- 다층 신경망에서 학습이 가능하다.
- 가중치와 편향을 업데이트하는데 효율적이며, 복잡한 모델에서도 적용할 수 있다.
- 그래디언트 계산을 통해 각 입력 변수의 중요도를 추정할 수 있다.

### 3.2 😅Cons
- 그래디언트 소실 문제: 역전파 동안 그래디언트가 소멸하거나 폭발할 수 있다.
- 계산 그래프의 크기에 따라 메모리 사용량이 증가할 수 있다.
- 신경망의 초기 가중치에 따라 결과가 달라질 수 있다.



_끝_