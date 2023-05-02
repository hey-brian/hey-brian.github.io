---
title: Boosting
feed: show
date : 2023-04-27
tags : [📝️/🌲️, ML]
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
- 약한 학습자(Weak learner)를 강한 학습자(Strong learner)로 변환하는 기계 학습 알고리즘의 집합
- 이진 분류를 위한 Boosting 알고리즘 중 가장 대표적이고 효과적인 알고리즘이 [[AdaBoost]]

### 1.2 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Boosting_(machine_learning))

# 2. How It Works
### 2.1 🔑Key 
- 기계 학습에서 부스팅(Boosting)은 앙상블 메타 알고리즘으로, 지도 학습에서 편향을 주로 줄이고 분산도 줄이는 데 사용되는 기계 학습 알고리즘의 일종이다. 
	- **약한 학습자(Weak learner)**: 무작위로 추측하는 것보다는 아주 살짝 더 성능이 좋은 분류기
	- **강한 학습자(Strong learner)**: 성능이 좋은 분류기
- 개념 논의의 시작: Kearns와 Valiant의 "다수의 약한 학습자가 모인 집합이 하나의 강한 학습자가 될 수 있는가?"(1988, 1989)
- 그에 대한 대답: 1990년에 Robert Schapire가 긍정적인 대답 = Boosting 개념 등장 + 기계 학습, 통계학에 영향
- 초기에 소개된 가설 부스팅 문제는 약한 학습자를 강한 학습자로 **변환**하는 과정을 의미했다.
	- *"Informally, the hypothesis boosting problem asks whether an efficient learning algorithm … that outputs a hypothesis whose performance is only slightly better than random guessing, i.e. a weak learner, implies the existence of an efficient algorithm that outputs a hypothesis of arbitrary accuracy, i.e. a strong learner."*

![](attachments/Pasted_image_20230428091750_watermarked.jpeg)

(\### image from [Wikipedia](https://en.wikipedia.org/wiki/Boosting_(machine_learning)))

# 3. Application
- [[AdaBoost]]


_끝_