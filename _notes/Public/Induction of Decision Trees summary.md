---
title: Induction of Decision Trees summary
feed: hide
date : 2023-03-29
time : 07:20:59
tags : [summary]
format: list
comments: true
---


![](/attachments/Screenshot_2023-03-29_at_72329_AM_watermarked.jpeg)

(\### image from [Induction of Decision Trees(1986)](https://link.springer.com/article/10.1007/BF00116251))

Decision Trees는 반복적으로 데이터를 분할하여 (나무 형태로 표현되는) '의사 결정 규칙'을 생성하는 머신 러닝 방법이다. 논문에서는 분류 문제를 해결하는 머신러닝 알고리즘 중 하나인 결정 트리의 개념, 생성 및 활용 방법에 대해 설명하고 있다. 

# Key Insights and Lessons Learned
- 결정 트리 알고리즘은 간단하고 직관적인 모델링 방법이며, 데이터 전처리 및 파라미터 조정이 적은 경우에도 높은 예측 성능을 보일 수 있다.
- **정보 이득, 지니 불순도** 등을 사용하여 데이터의 속성을 분할하고 결정 규칙을 생성할 수 있다.
	- 불순도를 최소화하는 것을 목표로 하는 알고리즘들은 결정 트리에서도 중요하게 활용된다.
- 결정 트리 모델의 과적합 문제를 해결하기 위해 가지치기 및 사후 **가지치기** 등의 기법을 사용할 수 있다.
- 결정 트리 모델은 이해하기 쉬운 구조로 인해, 의사 결정 과정을 설명하고 **모델의 해석력**을 높일 수 있다.
	- 결정 트리는 데이터의 특징 중요도를 파악할 수 있어 문제를 해결하는데 유용하다.
- 결정 트리 알고리즘은 다른 머신 러닝 알고리즘과 조합하여 앙상블 모델을 만들 수 있다.

# Related papers
1. Breiman, L., Friedman, J., Stone, C. J., & Olshen, R. A. (1984). Classification and regression trees.
2. Quinlan, J. R. (1993). C4. 5: Programs for machine learning.
3. Hastie, T., Tibshirani, R., & Friedman, J. (2009). The elements of statistical learning: data mining, inference, and prediction.
4. Bishop, C. M. (2006). Pattern recognition and machine learning.


_끝_