---
title: GAN summary
feed: show
date : 2022-12-28
tags : [📝️/🌲️, ML, DL]
comments: true
---

# 1. Training
- 데이터를 바탕으로 input -> model -> output 과정에서 model이 probability distribution을 학습할 수 있도록(=minimize a loss function) algorithm이 model's parameters 조정

# 2. Generative models vs. discriminative models
### 2.1 discriminative models
- supervised classification, regression에 사용되는 모델: NN, logistic regression, SVM, etc.
- 정해진 개수의 label로 구성된 labeled data를 사용
- training data에서 label을 나누는 경계(boundaries, P(y\|x))를 학습하고, 그 경계를 사용하여 예측 수행

### 2.2 generative models
- unsupervised learning model: Boltzmann machines, Variational AutoEncoder, HMM, GPT-2, etc.
- unlabeld data를 주로 사용
- 주어진 데이터셋(x 분포)이 어떤 확률모델(P(x))로부터 어떻게 생성될 수 있었는지를 학습, 모델을 sampling하여(stocastic, or random element 입력) 새로운 데이터를 생성
	+ latent space(데이터의 특성을 압축해놓은 vector represenation)에서 random data를 선택하여 generative model에 입력하고, 그 결과 model은 새로운 데이터 생성(Generated sample)

# 3. GAN (Generative Adversarial Networks)
- 데이터의 분포를 모방하여 데이터를 생성할 수 있는 Machine Learning 알고리즘
- 알고리즘을 구성하는 두 축(generator, discriminator)이 서로 경쟁하며 알고리즘이 학습됨. 
- 2014년 [NeurIPS paper](https://papers.nips.cc/paper/5423-generative-adversarial-nets.pdf)를 통해 발표 (저자: Ian Goodfellow 외)
  ###### \=\+\= image from [google developers](https://developers.google.com/machine-learning/gan/gan_structure)![](/attachments/Screenshot_2022-12-29_at_81037_AM_watermarked.png)
- 구조
	+ Generator: (discriminator가 속을 수 있을만한) 가짜 데이터를 생성하기 위해 학습 (GAN 명칭에서 Generative)
		* 다양한 알고리즘 선택 가능: input dimension=latent space dimension, output dimension=real data dimension인 다양한 알고리즘(MLP, CNN, etc) 사용가능
	+ Discriminator: 진짜 데이터와 (generator가 생성한)가짜 데이터를 판별하기 위해 학습 (GAN 명칭에서 Adversarial)
		* generator와 마찬가지로 input, output dimension만 맞다면 다양한 알고리즘 사용 가능
- 학습
	+ 두 players가 참여하는 minimax game
		* D는 진짜 데이터와 가짜 데이터(G 결과) 사이를 구별하는 error를 최소화
		* G는 D가 오판할 확률을 최대화
	+ D는 supervised learning과 닮았다.
		* 입력: 진짜 데이터와 가짜 데이터가 random하게 입력
		* 출력: 진짜 데이터(label:1) vs. 가짜 데이터(label:0)
		* Unlabeld data를 사용하는 unsupervised learning이지만, 진짜 데이터와 가짜 데이터를 구분하는 과정은 supervised learning처럼 보인다.
		  ###### \=\+\= image by author ![](/attachments/Screenshot_2022-12-29_at_80330_AM_watermarked.png)
		* 논문에서는 D 성능을 높이는데 더 집중
			- D의 parameters가 다회 update될 때, G의 parameters는 한 번 update된다.
			- D의 parameters가 update 완료된 이후, G를 학습하여 parameters를 update한다.
	+ (D 학습이 일단락되면) G를 학습한다. 
		* 전체적으로 보면, G를 학습할 때의 GAN도 단순한 classification 구조로 볼 수 있다.
			- 입력: random data w/ label 1 (generated sample labels을 1로 고정) 
			- 출력: classifiaction result = 진짜 데이터로 오판할(label: 1) 확률
			  ###### \=\+\= image by author![](/attachments/Screenshot_2022-12-29_at_80338_AM_watermarked.png)
		* G가 D를 속일 수 있을 정도로 훌륭하다면, D는 1에 가까운 값을 출력한다.
	+ *D와 G 학습 결과*
		* **학습이 진행될 수록(D와 G의 parameters가 update될수록), G는 진짜 데이터와 거의 비슷한 가짜 데이터를 생성하게 된다.**
		* **그 결과, D는 진짜 데이터와 G가 생성한 가짜 데이터를 거의 구별하지 못 하게 된다.**


_끝_
