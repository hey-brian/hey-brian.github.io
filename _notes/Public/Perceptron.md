---
title: Perceptron
feed: show
date : 2023-06-20
time : 07:37:03
tags : []
format: list
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
- 이진 분류 문제를 해결하기 위한 선형 분류 알고리즘

### 1.2 🎓Paper summary
- [[The Perceptron_A Probabilistic Model for Information Storage and Organization in The Brain summary]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Backpropagation)

# 2. How It Works
### 2.1 🔑Key 
- 입력과 가중치를 곱하여 합을 계산하고, 활성화 함수를 적용하여 예측
- 계산된 예측 값과 실제 값의 차이를 이용하여 가중치 조정
- 이러한 과정을 반복하여 최적의 가중치 탐색

![](/attachments/Pasted_image_20230622071431_watermarked.jpeg)

(\### image from [Wikipedia](https://en.wikipedia.org/wiki/Perceptron))

![](/attachments/Pasted_image_20230622071449_watermarked.jpeg)

(\### image from [Wikipedia](https://en.wikipedia.org/wiki/Perceptron))

# 3. Pros and Cons
### 3.1 😄Pros
- 간단하고 이해하기 쉽다.
- 선형 분리 가능한 문제에 대해 효과적으로 동작
- 가중치를 조정하여 데이터를 잘 분류하는 경계 학습 가능

### 3.2 😅Cons
- 비선형 분리 가능한 문제에 대해서는 비정상 작동 가능
- 수렴하지 않거나 학습 불가(큰 오차) 가능
- 과적합(overfitting) 발생 가능



_끝_