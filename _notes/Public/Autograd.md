---
title: Autograd
feed: show
date : 2023-06-13
time : 07:38:03
tags : []
format: list
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
- Autograd는 자동 미분(automatic differentiation)을 제공하는 라이브러리로, 딥 러닝에서 그래디언트 계산을 자동으로 처리하는 기능을 제공한다.

### 1.2 🎓Paper summary
- [[Autograd_Effortless Gratients in Numpy summary]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Automatic_differentiation)


# 2. How It Works
### 2.1 🔑Key 
> Backpropagation 계산을 위해 필요한 gradient(그래디언트)를 자동으로 계산

### 2.2 ⛓️Steps 
1. **계산 그래프 구성**: 사용자가 정의한 연산들로 계산 그래프를 구성한다.
2. **전진 패스**: 입력 데이터를 계산 그래프에 전달하여 중간 결과를 계산한다.
3. **역전패스 (Backpropagation)**: 전진 패스에서 구한 결과를 바탕으로 그래디언트를 역전패스하여 각 변수에 대한 미분 값을 계산한다.
4. **그래디언트 저장**(update): 계산된 그래디언트를 각 변수에 저장하여 후속 연산에 활용한다.

![](/attachments/Pasted_image_20230619071141_watermarked.jpeg)

(\### image from [Wikipedia](https://en.wikipedia.org/wiki/Automatic_differentiation))

![](/attachments/Pasted_image_20230619071304_watermarked.jpeg)

(\### image from [Wikipedia](https://en.wikipedia.org/wiki/Automatic_differentiation))


# 3. Pros and Cons
### 3.1 😄Pros
- 사용자가 직접 그래디언트를 계산하는 번거로움을 줄여준다.
- 복잡한 연산의 그래디언트를 효과적으로 계산할 수 있다.
- 동적 그래프 생성을 지원하여 모델 구성과 흐름을 유연하게 다룰 수 있다.
- 대부분의 텐서 연산 라이브러리와 호환되어 사용하기 편리하다.

### 3.2 😅Cons
- 메모리 사용량이 높을 수 있다.
- 계산 그래프 구성 및 그래디언트 계산에 일부 오버헤드가 발생할 수 있다.
- 일부 특정 연산에 대한 자동 미분이 지원되지 않을 수 있다.



_끝_