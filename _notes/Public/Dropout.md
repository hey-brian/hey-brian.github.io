---
title: Dropout
feed: show
date : 2023-04-27
tags : [📝️/🌲️, ML]
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
- 신경망의 과적합 문제를 완화하기 위해 학습 과정에서 일부 뉴런을 무작위로 비활성화하는 정규화 기법

### 1.2 🎓Paper summary
- [[Dropout_A Simple Way to Prevent Neural Networks from Overfitting summary]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Dilution_(neural_networks))

# 2. How It Works
### 2.1 🔑Key 
- 학습 과정에서 일부 뉴런을 랜덤하게 비활성화시켜 출력 값을 조정하고 가중치를 업데이트
- 비활성화된 뉴런은 신호를 전달하지 않으며, 이를 통해 다른 뉴런들이 독립적으로 학습
- 테스트 시에는 모든 뉴런을 사용하여 예측 수행

![](/attachments/Pasted_image_20230628071318_watermarked.jpeg)

(\### image from [Dropout: A Simple Way to Prevent Neural Networks from Overfitting(2014)](http://jmlr.org/papers/v15/srivastava14a.html))

# 3. Pros and Cons
### 3.1 😄Pros
- 과적합을 줄이고 모델의 일반화 성능을 향상 가능
- 신경망이 앙상블 효과를 가지게 되어 모델의 안정성 향상
- 계산 비용을 감소시키면서 모델의 효율성을 향상

### 3.2 😅Cons
- 학습 시에 비활성화된 뉴런들로 인해 효율 저하 가능
- 테스트 시에는 모든 뉴런을 사용하여 예측하므로 계산 비용이 증가 가능
- 일부 정보가 제거되기 때문에 작은 데이터셋에서는 성능 저하 발생 가능


_끝_