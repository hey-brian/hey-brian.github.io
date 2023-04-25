---
title: Bootstrap
feed: show
date : 2023-04-01
tags : [📝️/🌲️, ML]
comments: true
---

# 1. Introduction
### 1.1 ✂️TL;DR
Bootstrap은 표본으로부터 모집단의 특성을 추정하는데 사용되는 재표본추출 방법으로, 임의 표본 추출을 통해 추출한 통계량을 이용하여 **샘플(표본) 데이터**로부터 **모집단의 통계량 분포**(관심 통계량의 추정값과 신뢰구간)를 추정하여 **모집단의 특성을 추정**하는 통계학적 방법이다. (핵심개념: 중심극한정리)

### 1.2 🎓Paper summary
- [[Problems in Plane Sampling summary]]
- [[Notes on Bias Estimation summary]]
- [[Bias and Confidence in Not-quite Large Samples summary]]
- [[Bootstrap Methods_Another Look at the Jackknife summary]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Bootstrapping_(statistics))


# 2. How It Works
### 2.1 🔑Key 

> 샘플링한 데이터로부터 `모집단의 통계량 분포`를 추정하여 `모집단의 특성`을 추정

### 2.2 🧬Features
- 부트스트랩(bootstrapping)은 통계학에서 사용되는 기법 중 하나로, 원천 데이터셋에서 복원추출(resampling with replacement)을 통해 많은 새로운 샘플들을 만드는 것을 의미한다.
- 이러한 새로운 샘플들은 원래 데이터셋이 추출된 모집단(population)의 속성(예: 평균, 분산, 신뢰구간)을 추정하는 데 사용된다.
- 부트스트랩은 모집단 분포가 알려지지 않거나 모델링하기 어려운 경우나 샘플 크기가 작은 경우 특히 유용하게 사용된다.
- 가설 검정과 회귀 분석과 같은 다양한 통계적 검정에도 적용되는 기법이다.
- Bootstrap의 결과는 표본 크기, 표본 분포 및 추정량과 같은 다양한 요인에 따라 영향을 받는다.

# 3. Pros and Cons
### 3.1 Pros
- 부트스트랩은 표본 크기가 작을 때 모집단 특성을 추정하는 데 특히 유용하며, 적은 계산 비용으로 적은 편향과 높은 정확도를 가지는 추정치를 얻을 수 있다. 
- Bootstrap은 모집단의 분포나 모수에 대한 가정 없이 표본 데이터에서 통계량을 추정할 수 있다.
- Bootstrap은 이론적으로 유효한 추정값과 신뢰 구간을 제공하며, 이는 모집단 분포에 대한 지식이 부족한 경우에도 유용하다.
- Bootstrap은 모수적인 방법과 비모수적인 방법 모두에 적용할 수 있다.
- Bootstrap은 다양한 통계적 문제에 적용 가능하며, 예를 들어 회귀 분석, 분류 문제, 클러스터링 등에서 활용된다.

### 3.2 Cons
- 부트스트랩은 샘플 데이터가 모집단 분포를 대표하는 경우에만 적용할 수 있으며, 자료에 따라 부트스트랩 결과가 크게 달라질 수 있다는 한계점도 있다.

# 4. 관련 문서
- Efron, B. (1979). Bootstrap methods: another look at the jackknife. The annals of statistics, 7(1), 1-26.
- Davison, A. C., & Hinkley, D. V. (1997). Bootstrap methods and their application (Vol. 1). Cambridge university press.
- Hastie, T., Tibshirani, R., & Friedman, J. (2009). The elements of statistical learning: data mining, inference, and prediction. Springer Science & Business Media.
- James, G., Witten, D., Hastie, T., & Tibshirani, R. (2013). An introduction to statistical learning (Vol. 112). New York: springer.
- Shao, J., & Tu, D. (1995). The jackknife and bootstrap (Vol. 48). Springer Science & Business Media.

_끝_