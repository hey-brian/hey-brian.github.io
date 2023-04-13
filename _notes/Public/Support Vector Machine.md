---
title: Support Vector Machine
feed: show
date : 2023-03-31
tags : [📝️/🌲️, ML]
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
- SVM(Support Vector Machine)은 지도 학습 알고리즘 중 하나로, 주어진 데이터를 바탕으로 패턴을 분류하거나 예측
- SVM은 데이터를 분류하기 위해 결정 경계(decision boundary)를 찾는 방식으로 동작
### 1.2 🎓Paper summary
- [[Support Vector Networks summary]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Support_vector_machine)

# 2. How It Works
### 2.1 🔑Key 
- 두 클래스의 `p`차원 데이터 포인트를 최대한 잘 구분하는 `p-1`차원decision boundary(초평면)을 찾는 것

### 2.2 ⛓️Steps ``
- decision boundary는 데이터를 분리하는 최대한 넓은 간격(margin)을 유지하는 것이 목적이며 이를 위해 서포트 벡터(support vector)를 사용한다. 
- support vector는 decision boundary와 가장 가까이 있는 데이터 포인트들을 의미

(\### image from [wikipedia](https://en.wikipedia.org/wiki/Support_vector_machine#/media/File:Svm_separating_hyperplanes_(SVG).svg))

![](/attachments/svm_wikipedia.png)

- “최적”은 위 그림에서 검은공과 흰공으로 표시된 두 클래스 사이의 가장 큰 여백을 가진 초평면을 의미
	- H1: 클래스를 구분하지 못함.
	- H2: 클래스를 구분하지만 작은 여백
	- **H3: 클래스를 "최대 여백"으로 분류**

# 3. Pros and Cons
- 장점은 고차원 데이터에서도 잘 동작하며, 학습 데이터의 수가 적어도 성능이 좋은 편이다.
- 하지만 SVM은 데이터가 선형 분리 가능한 경우에만 적용이 가능하며, 커널 함수(kernel function)를 사용하여 비선형 분류를 수행할 수 있지만 커널 함수의 선택이나 매개변수의 조정이 필요하다.

# 4. Application
- SVM은 다양한 분야에서 활용되고 있으며, 이미지 처리, 텍스트 분류, 바이오 인포매틱스 등에서 먼저 시도해볼 수 있는 알고리즘이다. 



_끝_
