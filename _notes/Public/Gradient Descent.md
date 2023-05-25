---
title: Gradient Descent
feed: show
date : 2023-05-25
tags : [📝️/🌲️, ML]
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
- 함수의 기울기 정보를 이용하여 loss function의 최소값을 찾아가며 최적화된 파라미터를 찾는 방법

### 1.2 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Gradient_descent)

# 2. How It Works
### 2.1 🔑Key 

> 경사 하강법의 핵심 아이디어는 `함수의 기울기를 따라서 최소값으로 점진적으로 이동`

### 2.2 ⛓️Steps 
1.  초기에는 파라미터 값을 임의로 설정
2.  주어진 손실 함수의 기울기(gradient)를 계산
3.  그레디언트를 이용하여 파라미터를 업데이트. 업데이트는 기울기에 학습률(learning rate)을 곱한 값만큼 파라미터를 조정.
4.  2~3단계를 반복하여 손실 함수의 값이 최소화되는 파라미터 값 탐색

![](/attachments/Pasted_image_20230525071716_watermarked.jpeg)

(\### image from [Wikipedia](https://en.wikipedia.org/wiki/Gradient_descent))

# 3. Pros and Cons
### 3.1 Pros
- 다양한 종류의 함수에 적용 가능
- 수렴이 보장되는 경우에는 최적값 도달 가능

### 3.2 Cons
- 기울기에 따라 단순히 이동하기 때문에 지역 최소값에 갇힐 수 있다.
- 학습률 설정에 따라 수렴 속도와 성능이 달라짐.

# 4. Application
- [[Stochastic Gradient Descent]] 

_끝_