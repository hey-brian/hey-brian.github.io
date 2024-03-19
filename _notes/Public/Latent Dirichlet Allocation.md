---
title: Latent Dirichlet Allocation
feed: show
date : 2023-07-27
time : 07:24:03
tags : []
format: list
comments: true
---
	
# 1. Introduction
### 1.1 ✂️TL;DR
- Latent Dirichlet Allocation (LDA)는 주제 모델링(topic modeling) 기법 중 하나로, 텍스트 데이터에서 숨겨진 토픽들을 추출하는 알고리즘

### 1.2 🎓Paper summary
- [[Latent Dirichlet Allocation summary]]

### 1.3 🔗Useful links
- [Wikipedia](https://en.wikipedia.org/wiki/Latent_Dirichlet_allocation)


# 2. How It Works
### 2.1 🔑Key 
> 주어진 단어들의 패턴을 사용하여 문서들의 토픽 구성과 토픽의 단어 분포를 추정

### 2.2 ⛓️Steps 
1. 초기화: 주어진 문서 집합에 대해 토픽의 개수를 미리 설정하고, 각 문서의 단어들을 임의의 토픽에 할당한다.
2. 추정: LDA는 주어진 단어들의 발생 패턴을 바탕으로 문서들의 토픽 구성과 토픽들의 단어 분포를 추정한다. 이를 통해 숨겨진 토픽들을 추출해낼 수 있다.
	
	$$p(word\ with\ topic) = p(topic|document) * p(word|topic)$$
	- $$p(topic|document)$$
		- 문서 d에 할당된 단어들 중 주제 t에 속하는 단어의 비율 
		- 특정 문서 d에서 주제 t에 속하는 단어가 얼마나 많은지를 나타내며 현재 단어는 제외한다.
		- 만약 d에서 많은 단어들이 t에 속한다면, 단어 w가 t에 속하는 확률이 높아진다.
	- $$p(word|topic)$$
		- 모든 문서에서 주제 t에 할당된 비율 중, 단어 w에 의해 생성된 비율
		- 단어 w로 인해 주제 t에 속하는 문서가 얼마나 많은지를 나타냅니다.
	- LDA는 문서를 주제들의 혼합으로 표현하고 주제는 단어들의 혼합이다. 만약 어떤 단어가 특정 주제에 높은 확률로 속한다면, 해당 단어를 포함하는 모든 문서들도 주제 t와 강하게 연결된다. 마찬가지로 만약 w가 t에 속할 확률이 낮다면, w를 포함하는 문서들은 높은 확률로 다른 주제로 연결될 것이다. (주제 t와 연결은 약하다.)
3. 반복 학습: LDA는 반복적인 학습 과정을 거치면서 토픽 구성과 단어 분포를 조정한다. 이때 Gibbs 샘플링과 같은 MCMC(Markov Chain Monte Carlo) 알고리즘을 사용하여 추정을 수행한다.
4. 수렴: 학습이 충분히 진행된 후, LDA는 수렴 상태에 도달하여 최종적인 토픽 구성과 단어 분포를 얻는다.

![](/attachments/Pasted_image_20230727074249_watermarked.jpeg)
(\### image from [analyticsvidhya.com](https://www.analyticsvidhya.com/blog/2021/06/part-2-topic-modeling-and-latent-dirichlet-allocation-lda-using-gensim-and-sklearn/))

# 3. Pros and Cons
### 3.1 😄Pros
- 토픽 추출: LDA는 문서 집합에서 숨겨진 토픽들을 추출해내어 문서의 의미를 파악하는 데 유용하다.
- 차원 축소: LDA를 이용하여 텍스트 데이터를 토픽 공간으로 임베딩하면, 차원 축소 효과를 얻을 수 있다.
- 문서 군집화: LDA를 통해 유사한 주제를 갖는 문서들을 군집화하여 텍스트 분석에 활용할 수 있다.

### 3.2 😅Cons
- 사전 설정: 알고리즘에는 토픽 수와 같이 사전 설정해야 하는 하이퍼파라미터가 존재하여 이를 설정하는 단계가 필수적이.
- 단어 순서 무시: LDA는 문서 내 단어 순서를 무시하고 단어들 간 독립성을 가정한다. (현실성이 떨어지는 특성)

_끝_