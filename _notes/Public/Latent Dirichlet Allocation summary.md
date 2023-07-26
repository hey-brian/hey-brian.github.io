---
title: Latent Dirichlet Allocation summary
feed: hide
date : 2023-03-31
time : 07:32:14
tags : [summary]
format: list
comments: true
---

![](/attachments/Screenshot_2023-03-31_at_73402_AM_watermarked.jpeg)

(\### image from [Latent Dirichlet Allocation(2003)](http://jmlr.csail.mit.edu/papers/v3/blei03a.html))

"Latent Dirichlet Allocation" 논문은 문서들을 토픽(주제)으로 구분하고, "토픽을 구성하는 단어들을 확률 분포"로 각 문서를 모델링하는 확률적 생성 모델인 LDA를 제안하는 논문이다.

# Key Insights and Lessons Learned
- LDA는 문서 집합을 토픽 모델링에 활용하기 위한 확률적 생성 모델이다.
- LDA는 문서의 토픽의 출현 확률 분포와 각 토픽의 단어의 출현 확률 분포를 추정하며, 이를 통해 문서를 토픽의 조합으로 표현한다. 그리고 이 표현을 이용하여 새로운 문서의 토픽 분포와 단어 분포를 추정한다.
- LDA는 문서를 구성하는 단어들을 바탕으로 문서가 어떤 토픽으로 구성되어 있는지를 추론하는 확률적 모델로, 베이지안 추론을 기반으로 하여 모델의 파라미터를 추정한다.
- LDA는 단어의 순서 정보를 고려하지 않기 때문에, 문서의 의미를 완벽하게 파악하지 못할 수 있다.
- LDA는 자연어 처리 분야에서 토픽 모델링에 많이 사용되며, 다른 분야에서도 응용이 가능하다. (LDA를 통해 문서 집합에서 토픽을 추출하면, 문서를 토픽 단위로 분류하거나 새로운 문서의 토픽을 예측하는 등의 다양한 응용이 가능)

# Related papers
- Blei, D. M., Ng, A. Y., & Jordan, M. I. (2003). Latent Dirichlet allocation. Journal of machine Learning research, 3(Jan), 993-1022.
- Griffiths, T. L., & Steyvers, M. (2004). Finding scientific topics. Proceedings of the National academy of Sciences, 101(suppl 1), 5228-5235.
- Newman, D., Lau, J. H., Grieser, K., & Baldwin, T. (2010). Automatic evaluation of topic coherence. In Human Language Technologies: The 2010 Annual Conference of the North American Chapter of the Association for Computational Linguistics (pp. 100-108).
- Wang, C., Blei, D. M., & Li, F. F. (2009). Simultaneous image classification and annotation. In Computer Vision and Pattern Recognition, 2009. CVPR 2009. IEEE Conference on (pp. 1903-1910).

_끝_