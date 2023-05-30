---
title: Expectation Maximization
feed: show
date : 2023-05-30
time : 07:11:13
tags : []
format: list
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
- EM 알고리즘은 데이터의 불완전성이나 숨겨진 변수에 의존하는 경우에 사용되며, 확률 모델의 파라미터 추정에 사용되는 반복적인 최적화 알고리즘

### 1.2 🎓Paper summary
- [[Maximum likelihood from incomplete data via the EM algorithm summary]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Expectation%E2%80%93maximization_algorithm)

# 2. How It Works
### 2.1 🔑Key 

> "E(Expectation)" 단계와 "M(Maximization)" 단계를 반복하며, 파라미터 값을 점진적으로 최적화하여 모델을 학습

### 2.2 ⛓️Steps 
1. 초기에는 파라미터 값을 임의로 설정
2. `E단계(Expectation Step)`: E단계에서는 현재의 파라미터 값을 기반으로 숨겨진 변수에 대한 기대값(Expectation)을 추정한다. 기대값은 주어진 데이터와 파라미터를 기반으로 숨겨진 변수의 확률 분포를 계산하여 숨겨진 변수의 값에 대한 확률적 예측을 수행한다.
3. `M단계(Maximization Step)`: M단계에서는 E단계에서 계산한 숨겨진 변수의 기대값을 사용하여 파라미터를 최대화(Maximization)한다. 숨겨진 변수의 기대값을 사용하여 파라미터를 조정하여 주어진 데이터에 대한 가능도(likelihood)를 최대화하는 방향으로 파라미터 값을 업데이트한다.
4. 2~3단계를 반복하여 파라미터 값이 수렴할 때까지 반복한다.

![](/attachments/EM_Clustering_of_Old_Faithful_data.gif)

(\### image from [Wikipedia](https://en.wikipedia.org/wiki/Expectation%E2%80%93maximization_algorithm))

# 3. Pros and Cons
### 3.1 Pros
- 불완전한 데이터 또는 숨겨진 변수가 있는 경우에도 파라미터를 추정 가능
- 수렴이 보장되는 경우에는 국지적인 최적값에 도달 가능 

### 3.2 Cons
- 초기 파라미터 값에 민감하게 반응할 수 있다.
- 수렴 속도가 느릴 수 있다.

# 4. Application
- 클러스터링(Clustering): EM 알고리즘을 사용하여 데이터를 클러스터로 그룹화하는 경우, 각 클러스터는 특정한 확률 분포를 가지며, 데이터 포인트는 각 클러스터에 속할 확률을 가진다. (클러스터링: 유사한 속성을 가진 데이터 포인트를 그룹으로 그룹핑)
- 잠재 변수 모델(Latent Variable Models): 잠재 변수 모델은 데이터에 대한 부분적인 관찰만을 가지고 숨겨진(latent) 변수를 추정하는 모델이며, EM 알고리즘은 잠재 변수 모델의 파라미터 추정에 사용된다. 
	- 가우시안 혼합 모델(Gaussian Mixture Model)은 데이터를 여러 개의 가우시안 분포를 가진 클러스터로 모델링하는 잠재 변수 모델이며, 이 때 EM 알고리즘을 사용하여 가우시안 혼합 모델의 파라미터를 추정한다.
- 이미지 처리(Image Processing): 이미지 분할(image segmentation) 문제에서 EM 알고리즘은 이미지를 서로 다른 영역으로 분할하는 데 사용되는데, 각 영역은 특정한 확률 분포를 따르며 EM 알고리즘은 영역의 파라미터를 추정하여 이미지 분할을 수행한다.
- 데이터 복원(Data Imputation): EM 알고리즘을 사용하여 결측치가 있는 데이터의 잠재 변수와 파라미터를 동시에 추정하여 데이터를 복원할 수 있다. (결측치: 데이터에서 누락된 값이 존재)

_끝_